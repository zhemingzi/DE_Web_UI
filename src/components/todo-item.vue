<template>
  <div id="todoitemcomponent">
    <li>{{ todo.text }}</li>
  </div>
</template>

<script>

export default {
  props: ["todo"],
};
</script>

<style>
/* #app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
