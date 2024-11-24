<template>
  <div class="ocean1-main">
    <div class="ocean1-title">
      <img
        src="../assets/title2.png"
        alt=""
        style="height: 50px; width: 100%"
      />
    </div>
    <div class="ocean1-bar">
      <img
        src="../assets/bar2.jpg"
        alt=""
        style="
          position: relative;
          height: 100%;
          width: 100%;
          /* border-radius: 10% 10% 10% 10%; */
        "
      />
      <img
        src="../assets/菜单.jpg"
        alt=""
        style="
          position: relative;
          bottom: 214px;
          left: 44px;
          height: 210px;
          width: 300px;
          border-radius: 0px 30px 30px 0px;
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
  background: linear-gradient(rgb(34, 132, 217), rgb(192, 253, 255));
  height: 50px;
}

.ocean1-bar {
  position: relative;
  text-align: center;
  top: -50px;
  height: 740px;
  width: 40px;
  background: transparent;
}

.ocean1-panel {
  height: 480px;
  position: absolute;
  top: 5%;
  left: 45px;
  height: 480px;
  width: 180px;
  background: transparent;
}
</style>
