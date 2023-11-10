<template>
  <div class="block" v-if="showBlock" @click="stopTimer">Click me!</div>
</template>

<script>
export default {
  props: ["delay"],
  data() {
    return {
      showBlock: false,
      timer: null,
      reactionTime: 0,
    };
  },
  mounted() {
    // args: callback, delay
    setTimeout(() => {
      this.showBlock = true;
      this.startTimer();
    }, this.delay);
  },
  methods: {
    // every 10ms add 10ms to reactionTime
    startTimer() {
      this.timer = setInterval(() => {
        this.reactionTime += 10;
      }, 10);
    },
    stopTimer() {
      clearInterval(this.timer);
      // emit event with data
      this.$emit("end", this.reactionTime);
    },
  },
};
</script>

<style>
.block {
  width: 400px;
  border-radius: 20px;
  background: rgb(253, 0, 0);
  color: white;
  text-align: center;
  padding: 100px 0;
  margin: 50px auto;
}
</style>
