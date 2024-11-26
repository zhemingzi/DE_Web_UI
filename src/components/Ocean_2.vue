<template>
  <div class="ocean1-main">
    <div class="ocean1-title">
      <img
        src="../assets/Title/title1-1.png"
        alt=""
        style="height: 100%; width: 100%"
      />
      <img
        src="../assets/DO_Logo.png"
        style="position: absolute; top: -6%; left: 41%; width: 18%; height: 60%"
      />
      <RealTimeClock class="Time"></RealTimeClock>
      <img
        src="../assets/Icon/17-icon.png"
        style="
          position: absolute;
          bottom: 42%;
          right: 18%;
          width: 40px;
          height: 40px;
        "
      />
      <img
        src="../assets/Icon/18-icon.png"
        style="
          position: absolute;
          bottom: 42%;
          right: 15%;
          width: 40px;
          height: 40px;
        "
      />
      <img
        src="../assets/Icon/8-icon.png"
        style="
          position: absolute;
          bottom: 42%;
          right: 12%;
          width: 40px;
          height: 40px;
        "
      />
      <img
        src="../assets/Icon/9-icon.png"
        style="
          position: absolute;
          bottom: 42%;
          right: 9%;
          width: 40px;
          height: 40px;
        "
      />
    </div>
    <div class="ocean1-bar">
      <img
        src="../assets/Sidebar/测边框1-3.png"
        style="
          position: absolute;
          top: -50px;
          left: 0%;
          width: 64px;
          height: 800px;
        "
      />
      <img
        src="../assets/Icon/24-六边形-1.png"
        style="
          position: absolute;
          top: -30px;
          left: 7%;
          width: 55px;
          height: 55px;
        "
      />
      <img
        src="../assets/Icon/24-六边形.png"
        style="
          position: absolute;
          top: 30px;
          left: 7%;
          width: 55px;
          height: 55px;
        "
      />
      <img
        src="../assets/Icon/24-六边形.png"
        style="
          position: absolute;
          top: 90px;
          left: 7%;
          width: 55px;
          height: 55px;
        "
      />
      <img
        src="../assets/Icon/24-六边形.png"
        style="
          position: absolute;
          top: 150px;
          left: 7%;
          width: 55px;
          height: 55px;
        "
      />
    </div>
    <div class="ocean1-panel" style="">
      <img src="../assets/Panel/3-边框.png" style="width: 100%; height: 100%" />
      <p
        style="
          position: absolute;
          font-size: 20px;
          color: rgba(255, 255, 255, 255);
          top: 5.5%;
          left: 10%;
        "
      >
        CTD面板
      </p>
      <div class="box"></div>
      <div class="boxx"></div>
    </div>
  </div>
</template>

<script>
import RealTimeClock from "./Time.vue";
export default {
  name: "Ocean1",
  components: { RealTimeClock },
  data() {
    return {};
  },
  mounted() {},
  methods: {},
};
</script>

<style>
.ocean1-main {
  position: relative;
}
.ocean1-title {
  position: relative;
  /* background: linear-gradient(rgb(34, 132, 217), rgb(192, 253, 255)); */
  height: 140px;
}

.Time {
  position: absolute;
  bottom: 45%;
  left: 6%;
  font-size: 22px;
  color: #59def3f6;
}
.ocean1-bar {
  position: relative;
  text-align: center;
  height: 100%;
  width: 60px;
  background: transparent;
}

.ocean1-panel {
  position: relative;
  top: 30%;
  left: 20%;
  width: 500px;
  height: 320px;
  background: transparent;
}
@keyframes animated-border {
  0% {
    box-shadow: 0 0 0 0 rgba(134, 211, 230, 1);
  }
  100% {
    box-shadow: 0 0 0 20px rgba(255, 255, 255, 0);
  }
}
.box {
  animation: animated-border 1.5s infinite;
  font-family: Arial;
  font-size: 18px;
  line-height: 30px;
  font-weight: bold;
  color: rgb(14, 199, 232);
  border: 2px solid;
  padding: 15px;
  border-radius: 10% 10% 10% 10%;
}
.boxx {
  height: 100px;
  clip-path: polygon(
    6px 0,
    calc(100% - 6px) 0,

    100% 6px,
    100% calc(100% - 6px),
    calc(100% - 6px) 100%,
    6px 100%,

    0 calc(100% - 6px),
    0 6px
  );

  background: linear-gradient(-45deg, #287eef 4px, #0c4e81 0) bottom right,
    linear-gradient(45deg, #289eef 4px, #0c4e81 0) bottom left,
    linear-gradient(135deg, #289eef 4px, #0c4e81 0) top left,
    linear-gradient(-135deg, #289eef 4px, #0c4e81 0) top right;
  background-size: 50% 51%;

  background-repeat: no-repeat;

  border: solid 2px #289eef;
}
</style>
