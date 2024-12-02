<template>
  <div>
    <input type="range" id="rangeslinder" ref="inputDom" @input="func" />
    <!-- <div id="h4-container">
      <div id="h4-subcontainer">
        <h4>{{ rangePercent }}<span></span></h4>
      </div>
    </div> -->
  </div>
</template>

<script>
export default {
  name: "RangeSlinder",
  data() {
    return {
      // rangeNow: 0,
      // rangeMax: 0,
    };
  },
  methods: {
    func(event) {
      // $('[type="range"]').on("change input", function () {
      //   rangePercent = $('[type="range"]').val();
      //   $("h4").html(rangePercent + "<span></span>");
      //   $('[type="range"], h4>span').css(
      //     "filter",
      //     "hue-rotate(-" + rangePercent + "deg)"
      //   );
      //   $("h4").css({
      //     transform: "translateX(-50%) scale(" + (1 + rangePercent / 100) + ")",
      //     left: rangePercent + "%",
      //   });
      // });
      const slider = document.getElementById("rangeslinder");
      const rangeMax = this.$refs.inputDom.max;
      const rangeNow = this.$refs.inputDom.value;
      const rangePercent = calc(rangeNow / rangeMax);
      const changeDeg = calc(rangePercent * 180);
      slider.style.filter = "hue-rotate(${changeDeg}deg)";
    },
  },
  created() {
    this.function();
  },
};
</script>

<style scoped>
/* .h4 {
  color: #999;
  font-weight: 500;
  &:after {
    content: "%";
    padding-left: 1px;
  }
} */
.input[type="range"] {
  -webkit-appearance: none;
  appearance: none;
  outline: 0;
  border: 0;
  border-radius: 500px;
  width: 400px;
  max-width: 100%;
  margin: 24px 0 16px;
  transition: box-shadow 0.2s ease-in-out;
}
.input[type="range"]::-webkit-slider-runnable-track {
  height: 40px;
  -webkit-appearance: none;
  color: #444;
  transition: box-shadow 0.2s ease-in-out;
}
.input[type="range"]::-webkit-slider-thumb {
  width: 40px;
  -webkit-appearance: none;
  height: 40px;
  cursor: ew-resize;
  background: #fff;
  box-shadow: -340px 0 0 320px #1597ff, inset 0 0 0 40px #1597ff;
  border-radius: 50%;
  transition: box-shadow 0.2s ease-in-out;
  position: relative;
}
.input[type="range"]:active::-webkit-slider-thumb {
  background: #fff;
  box-shadow: -340px 0 0 320px #1597ff, inset 0 0 0 3px #1597ff;
}
/* #h4-container {
  width: 400px;
  max-width: 100%;
  padding: 0 20px;
  box-sizing: border-box;
  position: relative;
  #h4-subcontainer {
    width: 100%;
    position: relative;
    h4 {
      display: flex;
      align-items: center;
      justify-content: center;
      position: absolute;
      top: 0;
      width: 40px;
      height: 40px;
      color: #fff !important;
      font-size: 12px;
      transform-origin: center -10px;
      transform: translateX(-50%);
      transition: margin-top 0.15s ease-in-out, opacity 0.15s ease-in-out;
      span {
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
        background-color: #1597ff;
        border-radius: 0 50% 50% 50%;
        transform: rotate(45deg);
        z-index: -1;
      }
    }
  }
} */
/* .input:not(:active) + #h4-container h4 {
  opacity: 0;
  margin-top: -50px;
  pointer-events: none;
} */
</style>
