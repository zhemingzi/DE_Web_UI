<template>
  <div class="ocean1-main">
    <div class="ocean1-title">
      <img
        src="../assets/title.jpg"
        alt=""
        style="height: 50px; width: 900px"
      />
      <img
        src="../assets/用户.jpg"
        alt=""
        style="
          position: absolute;
          top: 7.5px;
          left: 7.5px;
          height: 35px;
          width: 35px;
        "
      />
      <img
        src="../assets/右上角选项.jpg"
        alt=""
        style="
          position: absolute;
          top: 10px;
          right: 10px;
          height: 30px;
          width: 150px;
        "
      />
    </div>
    <div class="ocean1-bar">
      <img
        src="../assets/options.jpg"
        alt=""
        style="
          position: relative;
          top: 1%;
          height: 200px;
          width: 40px;
          /* border-radius: 10% 10% 10% 10%; */
        "
      />
      <img
        src="../assets/菜单选项.jpg"
        alt=""
        style="
          position: absolute;
          top: 95%;
          left: 50%;
          transform: translate(-50%, -50%);
          height: 40px;
          width: 40px;
          border-radius: 10% 10% 10% 10%;
        "
      />
    </div>
    <div class="ocean1-panel">
      <img
        src="../assets/panel.jpg"
        alt=""
        style="height: 100%; width: 100%; border-radius: 20px 0px 30px 0px"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "Ocean1",
  data() {
    return {};
  },
  components: {},
  mounted() {},
  methods: {},
};
</script>

<style>
.ocean1-main {
  position: relative;
  height: 690px;
}
.ocean1-title {
  position: relative;
  background: rgb(34, 132, 217);
  height: 50px;
}

.ocean1-bar {
  position: relative;
  text-align: center;
  height: 100%;
  width: 50px;
  background: rgb(34, 132, 217);
}

.ocean1-panel {
  height: 480px;
  position: absolute;
  top: 10%;
  left: 5%;
  width: 200px;
  background: transparent;
}
</style>
