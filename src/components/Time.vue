<template>
  <p>{{ formattedDate }}</p>
</template>

<script>
export default {
  name: "RealTimeClock",
  data() {
    return {
      now: new Date(),
    };
  },
  computed: {
    formattedDate() {
      const year = this.now.getFullYear();
      const month = this.padZero(this.now.getMonth() + 1);
      const day = this.padZero(this.now.getDate());
      const hour = this.padZero(this.now.getHours());
      const minute = this.padZero(this.now.getMinutes());
      const second = this.padZero(this.now.getSeconds());
      return `本地时间 `+` ${year}/${month}/${day} ${hour}:${minute}:${second}`;
    },
  },
  methods: {
    padZero(value) {
      return value < 10 ? `0${value}` : value;
    },
    updateDate() {
      this.now = new Date();
    },
  },
  created() {
    this.timer = setInterval(this.updateDate, 1000);
  },
  beforeDestroy() {
    clearInterval(this.timer);
  },
};
</script>

<style scoped>
p {
  color: #daf6ff;
  text-shadow: 0 0 20px rgba(10, 175, 230, 1), 0 0 20px rgba(10, 175, 230, 0);
}
</style>
