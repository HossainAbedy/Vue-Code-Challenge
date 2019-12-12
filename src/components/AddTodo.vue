<template>
  <div>
    <div class="add input-field col s12 z-depth-1">
      <div class="waves-effect waves-teal btn-flat">Add Todo</div>
      <form @submit="onSubmit">
          <div class="row">
            <div class="input-field col s10">
                <input id="last_name" type="text" class="validate" v-model="title">
                <label for="last_name">Add Todo</label>
             </div>
             <div class="input-field col s2">
                <input class="btn" type="submit" value="Submit">
             </div>
          </div>
      </form>
    </div>
  </div>
</template>

<script>
import { mapActions } from "vuex";
export default {
  name: "AddTodo",
  data() {
    return {
      title: ""
    };
  },
  methods: {
    ...mapActions(["addTodo"]),
    onSubmit(e) {
      e.preventDefault();
      this.addTodo(this.title);
    }
  }
};
</script>

<style scoped>
/* form {
  display: flex;
}
input[type="text"] {
  flex: 10;
  padding: 10px;
  border: 1px solid #41b883;
  outline: 0;
}
input[type="submit"] {
  flex: 2;
  background: #41b883;
  color: #fff;
  border: 1px #41b883 solid;
  cursor: pointer;
} */
</style>