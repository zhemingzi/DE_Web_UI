<template>
  <div class="ocean-main">
    <div class="ocean-title">这里使标题</div>
    <div class="ocean-bar">这里是侧边栏</div>
    <div class="ocean-panel">这里是弹窗</div>
  </div>
</template>

<script>
export default {
  name: "Ocean",
  data() {
    return {};
  },
  components: {},
  mounted() {},
  methods: {},
};
</script>

<style>
.ocean-main {
  height: 677px;
}
.ocean-title {
  background: red;
  height: 50px;
}

.ocean-bar {
  height: 100%;
  width: 50px;
  background: blue;
}

.ocean-panel {
  height: 300px;
  position: fixed;
  width: 200px;
  top: 83px;
  background: yellow;
  left: 73px;
}
</style>
