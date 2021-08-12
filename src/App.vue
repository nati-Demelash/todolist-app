<template>
  <div class="container">
    <Header />
    <Todos :todos="todos" />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Todos from "./components/Todos.vue";

export default {
  name: "App",
  components: {
    Header,
    Todos,
  },
  data() {
    return {
      todos: [],
    };
  },
  created() {
    this.todos = [
      {
        id: 1,
        text: "Learn vue js ",
        reminder: true,
      },
      {
        id: 2,
        text: "Appointment with doctor",
        reminder: true,
      },
      {
        id: 3,
        text: "Meet with friends ",
        reminder: false,
      },
    ];
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap");
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: "Poppins", sans-serif;
}
.container {
  max-width: 350px;
  margin: 30px auto;
  overflow: auto;
  min-height: 450px;
  border: 1px solid #fffacd;
  background: #fffacd;
  padding: 30px;
  border-radius: 5px;
}
</style>
