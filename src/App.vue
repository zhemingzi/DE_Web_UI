<template>
  <div id="app">
    <Ocean1 />
  </div>
</template>

<script>
import todoitemcomponent from "./components/todo-item.vue";
import Ocean1 from "./components/Ocean_1.vue";
export default {
  name: "App",
  data() {
    return {
      list: [
        { id: 0, text: "text1" },
        { id: 1, text: "text2" },
        { id: 2, text: "text3" },
      ],
    };
  },
  components: { todoitemcomponent, Ocean1 },
};
</script>

<style>
#app {
  height: 740px;
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #235f9a;
  background-color: #021227;
  margin: 0px;
  /* margin-top: 60px; */
}
</style>
