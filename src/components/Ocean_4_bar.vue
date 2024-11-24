<template>
  <div class="ocean1-main">
    <div class="ocean1-title">
      <img
        src="../assets/风格3-title.jpg"
        alt=""
        style="position: relative; height: 50px; width: 100%"
      />
    </div>
    <div
      class="ocean1-bar"
      style="
        position: relative;
        left: 0px;
        top: 0px;
        height: 1030px;
        background: transparent;
      "
    >
      <img
        src="../assets/风格3-Bar3.jpg"
        alt=""
        style="
          position: absolute;
          bottom: 0px;
          left: 0px;
          height: 780px;
          width: 580px;
          border-radius: 0px 25px 25px 0px;
        "
      />
      <img
        src="../assets/风格3-corner.jpg"
        alt=""
        style="
          position: absolute;
          bottom: 5px;
          right: 5px;
          height: 160px;
          width: 450px;
          border-radius: 10px 5px px 5px;
        "
      />
    </div>
    <!-- <div class="ocean1-panel">
      <img
        src="../assets/风格2-详细界面.jpg"
        alt=""
        style="height: 100%; width: 100%; border-radius: 20px 0px 30px 0px"
      />
    </div> -->
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
  height: 100%;
}
.ocean1-title {
  position: relative;
  height: 50px;
}

.ocean1-bar {
  position: relative;
  background: transparent;
}

.ocean1-panel {
  height: 480px;
  position: absolute;
  top: 5%;
  left: 200px;
  height: 480px;
  width: 180px;
  background: transparent;
}
</style>
