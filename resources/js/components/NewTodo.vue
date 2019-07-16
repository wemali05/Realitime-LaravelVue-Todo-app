    //../resources/js/components/NewTodo.vue
    <template>
         <input type="text" v-model="newTodo.title"
         @keyup.enter="addTodo" autofocus="autofocus"
          placeholder="What are you trying to get done?" class="new-todo">
    </template>
    <script>
    import { mapGetters } from "vuex";
    export default {
      name: "NewTodo",
      methods: {
        addTodo() {
          this.$store.dispatch("ADD_TODO", this.newTodo);
        }
      },
      computed: {
        ...mapGetters(["newTodo"])
      }
    };
    </script>
