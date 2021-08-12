<template>
  <div v-for="todo in todos" :key="todo.id">
      <h4>{{ todo.text }}</h4>
  </div>
</template>

<script>
export default {
  props: {
    todos: Array,
  },
};
</script>

<style scoped>
h4{
    padding:15px 7px;
}
</style>
