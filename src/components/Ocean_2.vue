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
        src="../assets/Sidebar/测边框1-4.png"
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

      <div class="panel1" style="width: 500px; height: 320px">
        <div class="panelBorderOuter">
          <div class="panelBorderInner">
            <div>
              <img
                src="../assets/Panel/TitleBar3.png"
                style="
                  position: absolute;
                  left: 12px;
                  top: 4px;
                  height: 32px;
                  width: 90%;
                "
              />
              <p
                style="
                  position: absolute;
                  font-size: 20px;
                  color: rgba(255, 255, 255, 255);
                  top: 8px;
                  left: 12%;
                "
              >
                CTD面板
              </p>
              <div
                class="words"
                style="position: relative; height: 200px; width: 480px"
              >
                <p
                  style="
                    position: absolute;
                    top: 200px;
                    left: 20px;
                    font-size: 20px;
                    color: rgb(255, 255, 255);
                    /* background-image: url('../assets/Panel/3-边框.png'); */
                    background-color: rgb(255, 255, 255, 255);
                  "
                >
                  测试文字CTD
                </p>
                <p
                  style="
                    position: absolute;
                    top: 100px;
                    left: 20px;
                    font-size: 20px;
                    color: rgb(255, 255, 255);
                    /* background-image: url('../assets/Panel/3-边框.png'); */
                    background-color: rgb(255, 255, 255, 255);
                  "
                >
                  测试文字CTD
                </p>
                <input id="slider" type="range" min="0" max="550" step="1"  style="position: absolute;top: 107px;right: 40px;width: 180px; "/>
              </div>
            </div>
          </div>
        </div>
      </div>
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
  animation: animated-border 4s infinite;
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
    box-shadow: 0 0 0 10px rgba(255, 255, 255, 0);
  }
}
@keyframes animated-border2 {
  0% {
    margin: auto;
    filter: drop-shadow(0px 0px 0px rgb(85, 195, 242));
  }
  100% {
    margin: auto;
    filter: drop-shadow(0px 0px 30px rgba(241, 245, 246, 0));
  }
  /* 100% {
    margin: auto;
    filter: drop-shadow(0px 0px 1px rgba(29, 199, 241,1));
  } */
}
.box {
  animation: animated-border2 3s infinite;
  font-family: Arial;
  font-size: 18px;
  line-height: 30px;
  font-weight: bold;
  color: rgb(14, 199, 232);
  border: 2px solid;
  padding: 15px;
  border-radius: 20px 40% 50% 10px;
}
.boxx {
  animation: animated-border2 5s infinite;
  height: 100px;
  clip-path: polygon(
    10px 0px,
    calc(100% - 10px) 0px,
    100% 10px,
    100% calc(100% - 10px),
    calc(100% - 10px) 100%,
    10px 100%,
    0px calc(100% - 10px),
    0px 10px
  );
  /* clip-path: border-box; */
  /* clip-path: polygon(10% 0, 100% 50%, 50% 100%, 0 50%); */

  background: linear-gradient(-45deg, #287eef 4px, #0c4e81 0) bottom right,
    linear-gradient(45deg, #289eef 4px, #0c4e81 0) bottom left,
    linear-gradient(135deg, #289eef 4px, #0c4e81 0) top left,
    linear-gradient(-135deg, #289eef 4px, #0c4e81 0) top right;
  background-size: 50% 51%;

  background-repeat: no-repeat;

  border: solid 2px #289eef;
}
.panel1 {
  position: relative;
  border-radius: 16px 16px 16px 16px;
  animation: animated-border 3s infinite;
}
.panelBorderOuter {
  position: relative;
  /* top: 0%;
  left: 0%; */
  clip-path: polygon(
    10px 0px,
    calc(100% - 10px) 0px,
    100% 10px,
    100% calc(100% - 10px),
    calc(100% - 10px) 100%,
    10px 100%,
    0px calc(100% - 10px),
    0px 10px
  );
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
  background: linear-gradient(
        -45deg,
        transparent 4px,
        #03dafe 4px,
        #03dafe 12px,
        transparent 0
      )
      bottom right,
    linear-gradient(
        45deg,
        transparent 0px,
        #03dafe 4px,
        #03dafe 12px,
        transparent 0
      )
      bottom left,
    linear-gradient(
        135deg,
        transparent 4px,
        #03dafe 4px,
        #03dafe 12px,
        transparent 0
      )
      top left,
    linear-gradient(
        -135deg,
        transparent 4px,
        #03dafe 4px,
        #03dafe 12px,
        transparent 0
      )
      top right,
    linear-gradient(0deg, #186abb 3px, transparent 0) bottom right,
    linear-gradient(0deg, #03dafe 3px, transparent 0) bottom left,
    linear-gradient(180deg, #03dafe 3px, transparent 0) top left,
    linear-gradient(180deg, #03dafe 3px, transparent 0) top right,
    linear-gradient(90deg, #03dafe 3px, #0587dee7 3px, transparent 0) bottom
      left,
    linear-gradient(90deg, #03dafe 3px, #179bf351 3px, transparent 120px) top
      left,
    linear-gradient(270deg, #03dafe 3px, #179bf351 3px, transparent 120px) bottom
      right,
    linear-gradient(270deg, #03dafe 3px, #179bf351 3px, transparent 120px) top
      right;

  background-repeat: no-repeat;
}
.panelBorderInner {
  position: relative;
  clip-path: polygon(
    10px 0px,
    calc(100% - 10px) 0px,
    100% 10px,
    100% calc(100% - 10px),
    calc(100% - 10px) 100%,
    10px 100%,
    0px calc(100% - 10px),
    0px 10px
  );
  width: calc(100% - 12px);
  height: calc(100% - 12px);
  background: linear-gradient(
        -45deg,
        transparent 4px,
        rgb(45, 205, 208) 4px,
        rgb(45, 205, 208) 10px,
        transparent 0
      )
      bottom right,
    linear-gradient(
        45deg,
        transparent 4px,
        rgb(45, 205, 208) 4px,
        rgb(45, 205, 208) 10px,
        transparent 0
      )
      bottom left,
    linear-gradient(
        135deg,
        transparent 4px,
        rgb(45, 205, 208) 4px,
        rgb(45, 205, 208) 10px,
        transparent 0
      )
      top left,
    linear-gradient(
        -135deg,
        transparent 4px,
        rgb(45, 205, 208) 4px,
        rgb(45, 205, 208) 10px,
        transparent 0
      )
      top right;
}
.words > p {
  width: 200px;
  height: 30px;
  background-image: url("../assets/Panel/4-文字底纹.png");
  background-size: 200px 30px;
}
</style>
