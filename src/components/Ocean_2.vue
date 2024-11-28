<template>
  <div class="ocean1-main">
    <div class="ocean1-title">
      <img src="../assets/Title/title1-1.png" alt="" style="height: 100%; width: 100%" />
      <img src="../assets/DO_Logo.png" style="position: absolute; top: -6%; left: 41%; width: 18%; height: 60%" />
      <RealTimeClock class="Time"></RealTimeClock>
      <img
        src="../assets/Icon/17-icon.png"
        style="position: absolute; bottom: 42%; right: 18%; width: 40px; height: 40px"
      />
      <img
        src="../assets/Icon/18-icon.png"
        style="position: absolute; bottom: 42%; right: 15%; width: 40px; height: 40px"
      />
      <img
        src="../assets/Icon/8-icon.png"
        style="position: absolute; bottom: 42%; right: 12%; width: 40px; height: 40px"
      />
      <img
        src="../assets/Icon/9-icon.png"
        style="position: absolute; bottom: 42%; right: 9%; width: 40px; height: 40px"
      />
    </div>
    <div class="bar" style="position: relative; left: 1px; top: 1%; width: 60px; height: 88%">
      <div class="barBorderOuter">
        <div class="barBorderInner"></div>
      </div>
    </div>
    <!-- newSidebar -->

    <div class="panel" style="position: absolute; top: 120px; left: 200px; width: 420px; height: 600px">
      <div class="panelBorderOuter">
        <div class="panelBorderInner">
          <div>
            <img
              src="../assets/Panel/TitleBar3.png"
              style="position: absolute; left: 12px; top: 4px; height: 32px; width: 380px"
            />
            <p style="position: absolute; font-size: 20px; color: rgba(255, 255, 255, 255); top: 8px; left: 14%">
              CTD面板
            </p>
            <div class="words" style="position: relative; height: 200px; width: 480px">
              <p style="position: absolute; top: 200px; left: 20px; font-size: 18px; color: rgb(255, 255, 255)">
                CTD测试文字
              </p>
              <p
                style="
                  position: absolute;
                  top: 100px;
                  left: 20px;
                  width: 110px;
                  height: 20px;
                  font-size: 14px;
                  color: rgb(255, 255, 255);
                "
              >
                CTD测试文字
              </p>
              <input
                id="slider"
                type="range"
                min="0"
                max="550"
                step="1"
                style="position: absolute; top: 107px; right: 40px; width: 180px"
              />
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
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
}
.ocean1-title {
  position: relative;
  /* background: linear-gradient(rgb(34, 132, 217), rgb(192, 253, 255)); */
  height: 10%;
}

.Time {
  position: absolute;
  bottom: 45%;
  left: 6%;
  font-size: 22px;
  color: #59def3f6;
}

@keyframes animated-border {
  0% {
    box-shadow: 0 0 0 0 rgba(134, 211, 230, 1);
  }
  100% {
    box-shadow: 0 0 0 10px rgba(255, 255, 255, 0);
  }
}
@keyframes animated-border-2 {
  0% {
    box-shadow: 0 0 0 0px rgba(134, 211, 230, 1), 0 0 0 0px rgba(134, 211, 230, 1), 0 0 0 0px rgba(134, 211, 230, 1);
  }
  25% {
    box-shadow: 0 0 0 5px rgba(134, 211, 230, 0.5), 0 0 0 0px rgba(134, 211, 230, 1), 0 0 0 0px rgba(134, 211, 230, 1);
  }
  50% {
    box-shadow: 0 0 0 10px rgba(134, 211, 230, 0), 0 0 0 5px rgba(134, 211, 230, 0.5), 0 0 0 0px rgba(134, 211, 230, 1);
  }
  75% {
    box-shadow: 0 0 0 10px rgba(134, 211, 230, 0), 0 0 0 10px rgba(134, 211, 230, 0), 0 0 0 5px rgba(134, 211, 230, 0.5);
  }
  100% {
    box-shadow: 0 0 0 10px rgba(134, 211, 230, 0), 0 0 0 10px rgba(134, 211, 230, 0), 0 0 0 10px rgba(134, 211, 230, 0);
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
.panel {
  position: relative;
  border-radius: 25px 25px 25px 25px;
  animation: animated-border-2 9s infinite;
  animation-timing-function: linear;
  /* animation: animated-border-2 4s infinite; */
}
.barBorderOuter {
  clip-path: polygon(
    0px 0px,
    calc(100% - 40px) 0px,
    100% 30px,
    100% calc(100% - 30px),
    calc(100% - 40px) 100%,
    0px 100%
  );
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, #167be1d4 0.5px, #05bbf8 1.5px, #05bbf8 4.5px, transparent 0) bottom left,
    linear-gradient(90deg, #167be1d4 0.5px, #05bbf8 1.5px, #05bbf8 4.5px, transparent 0) top left,
    linear-gradient(270deg, #167be1d4 0.5px, #05bbf8 1.5px, #05bbf8 4.5px, transparent 0) bottom right,
    linear-gradient(270deg, #167be1d4 0.5px, #05bbf8 1.5px, #05bbf8 4.5px, transparent 0) top right,
    linear-gradient(0deg, #167be1d4 0.5px, #05bbf8 1.5px, #05bbf8 4.5px, transparent 0) bottom right,
    linear-gradient(0deg, #167be1d4 0.5px, #05bbf8 1.5px, #05bbf8 4.5px, transparent 0) bottom left,
    linear-gradient(180deg, #167be1d4 0.5px, #05bbf8 1.5px, #05bbf8 4.5px, transparent 0) top left,
    linear-gradient(180deg, #167be1d4 0.5px, #05bbf8 1.5px, #05bbf8 4.5px, transparent 0) top right,
    linear-gradient(-37deg, #05bbf8 28px, transparent 0) bottom right,
    /* linear-gradient(45deg, #05bbf8 13.5px, transparent 0) bottom left,
    linear-gradient(135deg, #05bbf8 13.5px, transparent 0) top left, */
      linear-gradient(-143deg, #05bbf8 28px, transparent 0);
  background-repeat: no-repeat;
}
.barBorderInner {
  position: relative;
  width: calc(100% - 13px);
  height: calc(100% - 12px);
  clip-path: polygon(
    0px 0px,
    calc(100% - 36px) 0px,
    100% 27px,
    100% calc(100% - 27px),
    calc(100% - 36px) 100%,
    0px 100%
  );
  background: 
  /* linear-gradient(180deg, #44ccee 2px, transparent 0), linear-gradient(0deg, #44ccee 2px, transparent 0), */
    linear-gradient(-37.5deg, #44ccee 27px, transparent 0), linear-gradient(-142.5deg, #44ccee 27px, transparent 0),
    linear-gradient(90deg, #1f84e9e7 0px, #0c60975d 60px);
}
.panelBorderOuter {
  position: relative;
  /* top: 0%;
  left: 0%; */
  clip-path: polygon(
    15px 0px,
    calc(100% - 15px) 0px,
    100% 15px,
    100% calc(100% - 15px),
    calc(100% - 15px) 100%,
    15px 100%,
    0px calc(100% - 15px),
    0px 15px
  );
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, #167be1d4 0.5px, #05bbf8 1.5px, #05bbf8 3.5px, transparent 0) bottom left,
    linear-gradient(90deg, #167be1d4 0.5px, #05bbf8 1.5px, #05bbf8 3.5px, transparent 0) top left,
    linear-gradient(270deg, #167be1d4 0.5px, #05bbf8 1.5px, #05bbf8 3.5px, transparent 0) bottom right,
    linear-gradient(270deg, #167be1d4 0.5px, #05bbf8 1.5px, #05bbf8 3.5px, transparent 0) top right,
    linear-gradient(0deg, #167be1d4 0.5px, #05bbf8 1.5px, #05bbf8 3.5px, transparent 0) bottom right,
    linear-gradient(0deg, #167be1d4 0.5px, #05bbf8 1.5px, #05bbf8 3.5px, transparent 0) bottom left,
    linear-gradient(180deg, #167be1d4 0.5px, #05bbf8 1.5px, #05bbf8 3.5px, transparent 0) top left,
    linear-gradient(180deg, #167be1d4 0.5px, #05bbf8 1.5px, #05bbf8 3.5px, transparent 0) top right,
    linear-gradient(-45deg, #05bbf8 13.5px, transparent 0) bottom right,
    linear-gradient(45deg, #05bbf8 13.5px, transparent 0) bottom left,
    linear-gradient(135deg, #05bbf8 13.5px, transparent 0) top left,
    linear-gradient(-135deg, #05bbf8 13.5px, transparent 0) top right;
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
  background: linear-gradient(-45deg, #44ccee 11px, #2e8ae593 11px, #2e8ae593 40px, #2e8ae56c 120px, transparent 300px)
      bottom right,
    linear-gradient(45deg, #44ccee 11px, #2e8ae593 11px, #2e8ae593 40px, #2e8ae56c 120px, transparent 300px) bottom left,
    linear-gradient(135deg, #44ccee 11px, #2e8ae593 11px, #2e8ae593 40px, #2e8ae56c 120px, transparent 300px) top left,
    linear-gradient(-135deg, #44ccee 11px, #2e8ae593 11px, #2e8ae593 40px, #2e8ae56c 120px, transparent 300px) top right;
}
.words > p {
  /* width: 180px;
  height: 30px; */
  background-image: url("../assets/Panel/9-文字底纹.png");
  background-size: 100% 100%;
}
</style>
