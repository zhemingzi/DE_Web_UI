<template>
  <div class="ocean1-main">
    <!-- Title -->
    <div class="ocean1-title">
      <img src="../assets/Title/title1-5.png" style="position: relative; top: 5%; height: 95%; width: 100%" />
      <h1>海洋可视化原型界面</h1>
      <h1>海洋可视化原型界面</h1>
      <img
        src="../assets/Icon/时间icon.png"
        title="时间"
        style="position: absolute; top: 48%; left: 66.5%; width: 28px; height: 24.2px"
      />
      <img
        src="../assets/Icon/工具icon.png"
        title="工具"
        style="position: absolute; top: 48%; left: 69%; width: 28px; height: 24.2px"
      />
      <img
        src="../assets/Icon/提示icon.png"
        title="提示"
        style="position: absolute; top: 48%; left: 71.5%; width: 28px; height: 24.2px"
      />
      <img
        src="../assets/Icon/搜索icon.png"
        title="搜索"
        style="position: absolute; top: 48%; left: 74%; width: 28px; height: 24.2px"
      />
      <img
        src="../assets/Icon/用户群icon.png"
        title="用户"
        style="position: absolute; top: 48%; left: 76.5%; width: 28px; height: 24.2px"
      />
      <img
        src="../assets/Icon/开机icon.png"
        title="关机"
        style="position: absolute; top: 48%; left: 79%; width: 28px; height: 24.2px"
      />
      <img
        src="../assets/DO_Logo.png"
        style="position: absolute; top: 12%; left: 37.5%; height: 70%; object-fit: contain"
      />
      <RealTimeClock style="position: absolute; top: 50%; left: 20%"></RealTimeClock>
    </div>
    <!-- Sidebar -->
    <div class="bar" style="position: relative; left: 1px; top: 1%; width: 60px; height: 88%">
      <div class="barBorderOuter">
        <div class="barBorderInner">
          <img
            src="../assets/Icon/路线-1icon.png"
            title="路线"
            style="position: relative; top: 40px; width: 40px; height: 40px"
          />
          <img
            src="../assets/Icon/温度icon.png"
            title="温度"
            style="position: relative; top: 55px; width: 40px; height: 40px"
          />
          <img
            src="../assets/Icon/灾害icon.png"
            title="灾害"
            style="position: relative; top: 70px; width: 40px; height: 40px"
          />
          <img
            src="../assets/Icon/海底地形icon.png"
            title="勘探"
            style="position: relative; top: 85px; width: 40px; height: 40px"
          />
          <img
            src="../assets/Icon/数据icon.png"
            title="数据"
            style="position: relative; top: 100px; width: 40px; height: 40px"
          />
        </div>
      </div>
    </div>

    <!-- Panel -->
    <div class="panel" style="position: absolute; top: 120px; left: 200px; width: 400px; height: 500px">
      <div class="panelBorderOuter">
        <div class="panelBorderInner">
          <div id="BarTitle" style="position: relative; height: 10%; width: 100%; pointer-events: none">
            <img
              src="../assets/Panel/标题底纹.png"
              style="position: absolute; left: 12px; top: 4px; height: 32px; width: 380px"
            />
            <p style="position: absolute; font-size: 20px; color: rgba(255, 255, 255, 255); top: 8px; left: 14%">
              CTD面板
            </p>
          </div>
          <div id="BarContent" style="position: relative; height: 90%; width: 100%">
            <div class="BarSelects" style="position: relative; height: 20%; width: 100%">
              <select
                name="data"
                id="dataSelect"
                style="text-overflow: ellipsis; position: absolute; top: 10%; left: 8%; width: 40%"
              >
                <option value="none" selected disabled hidden>选择数据</option>
                <option value="2017/11">2017年11月东海观测</option>
              </select>
              <select
                name="layer"
                id="layerSelect"
                style="text-overflow: ellipsis; position: absolute; top: 10%; right: 8%; width: 40%"
              >
                <option value="none" selected disabled hidden>选择层区</option>
                <option value="0-10">0-10层</option>
                <option value="11-20">11-20层</option>
                <option value="21-30">21-30层</option>
                <option value="31-40">31-40层</option>
                <option value="41-50">41-50层</option>
                <option value="51-60">51-60层</option>
                <option value="61-70">61-70层</option>
                <option value="71-80">71-80层</option>
                <option value="81-90">81-90层</option>
                <option value="91-100">91-100层</option>
              </select>
              <select
                name="kind"
                id="kindSelect"
                style="text-overflow: ellipsis; position: absolute; top: 50%; left: 8%; width: 40%"
              >
                <option value="none" selected disabled hidden>选择CTD数据</option>
                <option value="pressure">水压</option>
                <option value="temperature">温度</option>
                <option value="salty">盐度</option>
                <option value="density1">密度1</option>
                <option value="density2">密度2</option>
                <option value="oxygen">含氧量</option>
              </select>
              <select
                name="detailedkind"
                id="detailedKindSelect"
                style="text-overflow: ellipsis; position: absolute; top: 50%; right: 8%; width: 40%"
              >
                <option value="none" selected disabled hidden>选择详细种类</option>
                <option value="detailedsalty">营养盐数据</option>
                <option value="temperaturesalty">温盐数据</option>
              </select>
            </div>
            <div class="BarOptions" style="position: relative; height: 65%; width: 100%">
              <p style="position: absolute; top: 0%; left: 8%">默认配色</p>
              <p style="position: absolute; top: 15%; left: 8%">自定义颜色</p>
              <p style="position: absolute; top: 30%; left: 8%">颜色区间</p>
              <p style="position: absolute; top: 45%; left: 8%">透明度</p>
              <p style="position: absolute; top: 60%; left: 8%">颗粒大小</p>
              <p style="position: absolute; top: 75%; left: 8%">高度</p>
              <p style="position: absolute; top: 90%; left: 8%">层位</p>
              <img
                src="../assets/Panel/colorbar.png"
                style="position: absolute; top: 1%; left: 48%; width: 40%; height: 7%; border-radius: 8px"
              />
              <img
                src="../assets/Panel/colorbar.png"
                style="position: absolute; top: 16%; left: 48%; width: 40%; height: 7%; border-radius: 8px"
              />
              <input
                id="slider0"
                type="range"
                min="0"
                max="100"
                step="1"
                value="0"
                style="position: absolute; top: 32%; left: 48%; width: 44%"
              /><input
                id="slider1"
                type="range"
                min="0"
                max="100"
                step="1"
                value="0"
                style="position: absolute; top: 47%; left: 48%; width: 44%"
              />
              <input
                id="slider2"
                type="range"
                min="0"
                max="20"
                step="1"
                value="0"
                style="position: absolute; top: 62%; left: 48%; width: 44%"
              />
              <input
                id="slider2"
                type="range"
                min="0"
                max="20"
                step="1"
                value="0"
                style="position: absolute; top: 77%; left: 48%; width: 44%"
              />
              <input
                type="range"
                min="0"
                max="10"
                step="1"
                value="0"
                style="position: absolute; top: 92%; left: 48%; width: 44%"
              />
              <!-- <RangeSlinder
                style="position: absolute; top: 91%; right: 40px; width: 180px"
              >
              </RangeSlinder> -->
            </div>
            <div class="BarBottom" style="position: relative; height: 15%; width: 100%">
              <img
                src="../assets/Icon/点击icon.png"
                style="position: absolute; top: 25%; right: 44%; width: 40px; height: 34.6px"
                title="点击"
              />
              <img
                src="../assets/Icon/框选icon.png"
                style="position: absolute; top: 25%; right: 32%; width: 40px; height: 34.6px"
                title="框选"
              />
              <img
                src="../assets/Icon/刷新icon.png"
                style="position: absolute; top: 25%; right: 20%; width: 40px; height: 34.6px"
                title="刷新"
              />
              <img
                src="../assets/Icon/删除icon.png"
                style="position: absolute; top: 25%; right: 8%; width: 40px; height: 34.6px"
                title="删除"
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
import RangeSlinder from "./RangeSlinder.vue";
export default {
  name: "Ocean1",
  components: { RealTimeClock, RangeSlinder },
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
  height: 7%;
}
.ocean1-title h1 {
  position: absolute;
  top: 20%;
  left: 45.5%;
  font-size: 28px;
}
.ocean1-title h1:nth-child(2) {
  -webkit-text-stroke: 0.2px #17dff1;
  color: #fbfdfff5;
}

/* .ocean1-main img[title]:hover::after {
  content: attr(title);
  position: absolute;
  top: -100%;
  left: 0;
  z-index: 100;
  background-color: aquamarine;
  width: 250px;
} */
@keyframes animate-title-wave {
  0%,
  100% {
    clip-path: polygon(
      0% 60%,
      2% 52%,
      4% 46%,
      6% 42%,
      8% 40%,
      9% 39%,
      11% 39%,
      12% 40%,
      14% 42%,
      16% 46%,
      18% 52%,
      20% 60%,
      22% 68%,
      24% 74%,
      26% 78%,
      28% 80%,
      29% 81%,
      31% 81%,
      32% 80%,
      34% 78%,
      36% 74%,
      38% 68%,
      40% 60%,
      42% 54%,
      44% 50%,
      46% 47%,
      48% 445%,
      49% 44%,
      51% 44%,
      52% 45%,
      54% 47%,
      56% 50%,
      58% 54%,
      60% 60%,
      62% 68%,
      64% 64%,
      66% 84%,
      68% 88%,
      69% 90%,
      71% 90%,
      72% 88%,
      74% 84%,
      76% 78%,
      78% 70%,
      80% 60%,
      82% 50%,
      84% 42%,
      86% 36%,
      88% 32%,
      89% 30%,
      91% 30%,
      92% 32%,
      94% 36%,
      96% 42%,
      98% 50%,
      100% 60%,
      100% 100%,
      0% 100%
    );
  }

  50% {
    clip-path: polygon(
      0% 60%,
      2% 68%,
      4% 74%,
      6% 78%,
      8% 80%,
      9% 81%,
      11% 81%,
      12% 80%,
      14% 78%,
      16% 74%,
      18% 68%,
      20% 60%,
      22% 52%,
      24% 46%,
      26% 42%,
      28% 40%,
      29% 39%,
      31% 39%,
      32% 40%,
      34% 42%,
      36% 46%,
      38% 52%,
      40% 60%,
      42% 68%,
      44% 74%,
      46% 78%,
      48% 80%,
      49% 81%,
      51% 81%,
      52% 80%,
      54% 78%,
      56% 74%,
      58% 68%,
      60% 60%,
      62% 54%,
      64% 50%,
      66% 47%,
      68% 45%,
      69% 44%,
      71% 44%,
      72% 45%,
      74% 47%,
      76% 50%,
      78% 54%,
      80% 60%,
      82% 70%,
      84% 78%,
      86% 84%,
      88% 88%,
      89% 90%,
      91% 90%,
      92% 88%,
      94% 84%,
      96% 78%,
      98% 70%,
      100% 60%,
      100% 100%,
      0% 100%
    );
  }
}
.ocean1-title h1:nth-child(3) {
  color: #03c7f8d0;
  animation: animate-title-wave 6s ease-in-out infinite;
  /* animation-timing-function: linear; */
}
/* .Time {
  position: relative;
  bottom: 15%;
  left: 20%;
  font-size: 22px;
  color: #59def3f6;
} */

@keyframes animated-border {
  0% {
    box-shadow: 0 0 0 0 rgba(134, 211, 230, 1);
  }
  100% {
    box-shadow: 0 0 0 10px rgba(255, 255, 255, 0);
  }
}
@keyframes animated-border-wave {
  0% {
    box-shadow: 0 0 0 0px rgba(134, 211, 230, 1), 0 0 0 0px rgba(134, 211, 230, 1), 0 0 0 0px rgba(134, 211, 230, 1);
  }
  25% {
    box-shadow: 0 0 0 7.5px rgba(134, 211, 230, 0.5), 0 0 0 0px rgba(134, 211, 230, 1), 0 0 0 0px rgba(134, 211, 230, 1);
  }
  50% {
    box-shadow: 0 0 0 15px rgba(134, 211, 230, 0), 0 0 0 7.5px rgba(134, 211, 230, 0.5),
      0 0 0 0px rgba(134, 211, 230, 1);
  }
  75% {
    box-shadow: 0 0 0 15px rgba(134, 211, 230, 0), 0 0 0 15px rgba(134, 211, 230, 0),
      0 0 0 7.5px rgba(134, 211, 230, 0.5);
  }
  100% {
    box-shadow: 0 0 0 15px rgba(134, 211, 230, 0), 0 0 0 15px rgba(134, 211, 230, 0), 0 0 0 15px rgba(134, 211, 230, 0);
  }
}
@keyframes animated-border-3 {
  0% {
    margin: auto;
    filter: drop-shadow(0px 0px 0px rgb(85, 195, 242));
  }
  100% {
    margin: auto;
    filter: drop-shadow(0px 0px 30px rgba(241, 245, 246, 0));
  }
}

.panel {
  position: relative;
  border-radius: 25px 25px 25px 25px;
  animation: animated-border-wave 6s infinite;
  animation-timing-function: linear;
  /* animation: animated-border-2 4s infinite; */
}
.panel p {
  width: 110px;
  height: 20px;
  font-size: 14px;
  color: rgb(255, 255, 255);
}
.panel input[type="range"] {
  -webkit-appearance: none;
  appearance: none;
  outline: 0;
  border: 0;
  border-radius: 10px;
  width: 400px;
  max-width: 100%;
  transition: box-shadow 0.2s ease-in-out;
  overflow: hidden;
  height: 15px;
  background-color: #3b434796;
}
.panel input[type="range"]::-webkit-slider-thumb {
  -webkit-appearance: none;
  height: 15px;
  width: 15px;
  cursor: ew-resize;
  background: #fff;
  box-shadow: -110px 0 0 100px #1597ff, inset 0 0 0 40px #1597ff;
  border-radius: 50%;
  transition: box-shadow 0.2s ease-in-out;
  position: relative;
}
.panel input[type="range"]::-webkit-slider-runnable-track {
  -webkit-appearance: none;
  color: #444;
  transition: box-shadow 0.2s ease-in-out;
}
.panel input[type="range"]:active::-webkit-slider-thumb {
  background: #fff;
  box-shadow: -110px 0 0 100px #1597ff, inset 0 0 0 2px #1597ff;
}
.panel select {
  -webkit-appearance: none;
  appearance: button;
  background-color: #0a86d9;
  color: white;
  padding: 3px;
  border: none;
  font-size: 14px;
  box-shadow: 5px -3px 10px rgba(0, 208, 255, 0.98);

  outline: none;
}
.panel select option {
  -webkit-appearance: none;
  appearance: button;
  background-color: #0a86d9;
  color: white;
  padding: 3px;
  border: none;
  font-size: 14px;
  outline: none;
}
.panel select option:hover {
  background-color: #44525e;
}

.panel option {
  padding: 5px;
  background-color: #f9f9f9;
  color: #333;
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
  background: linear-gradient(90deg, #167be1d4 1px, #05bbf8 1.5px, #05bbf8 3.5px, transparent 0) bottom left,
    linear-gradient(90deg, #167be1d4 1px, #05bbf8 1.5px, #05bbf8 3.5px, transparent 0) top left,
    linear-gradient(270deg, #167be1d4 1px, #05bbf8 1.5px, #05bbf8 3.5px, transparent 0) bottom right,
    linear-gradient(270deg, #167be1d4 1px, #05bbf8 1.5px, #05bbf8 3.5px, transparent 0) top right,
    linear-gradient(0deg, #167be1d4 1px, #05bbf8 1.5px, #05bbf8 3.5px, transparent 0) bottom right,
    linear-gradient(0deg, #167be1d4 1px, #05bbf8 1.5px, #05bbf8 3.5px, transparent 0) bottom left,
    linear-gradient(180deg, #167be1d4 1px, #05bbf8 1.5px, #05bbf8 3.5px, transparent 0) top left,
    linear-gradient(180deg, #167be1d4 1px, #05bbf8 1.5px, #05bbf8 3.5px, transparent 0) top right,
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
  background: linear-gradient(-37.5deg, #44cceedb 27px, transparent 0),
    /* linear-gradient(180deg, #44ccee 2px, transparent 0), linear-gradient(0deg, #44ccee 2px, transparent 0), */
      linear-gradient(-142.5deg, #44cceedb 27px, transparent 0),
    linear-gradient(90deg, #1f84e9b6 0px, #0c5f973a 60px);
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
.BarOptions p {
  width: 120px;
  height: 24px;
  font-size: 16px;
  background-image: url("../assets/Panel/9-文字底纹.png");
  background-size: 100% 100%;
}
.BarBottom p {
  width: 60px;
  height: 24px;
  font-size: 16px;
  background-image: url("../assets/Panel/9-文字底纹.png");
  background-size: 100% 100%;
}
</style>
