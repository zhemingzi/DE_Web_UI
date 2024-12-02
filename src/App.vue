<template>
  <div id="app">
    <Ocean1 />
  </div>
</template>

<script>
// import todoitemcomponent from "./components/todo-item.vue";
import Ocean1 from "./components/Ocean_2.vue";

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
  components: { Ocean1 },
};
</script>


<!-- 下面各个背景图片用于测试观感效果 -->
<style>
#app {
  position: relative;
  width: 1600px;
  height: 900px;
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #235f9a;
  /* background-color: #03101d; */
  background-image: url('./assets/Background/1-背景.png');
  /* background-image: url('./assets/Background/2-背景.png'); */
  /* background-image: url('./assets/Background/3-背景.png'); */
  background-size: 1600px 900px;
  margin: 0px;
  /* margin-top: 60px; */
}
</style>
