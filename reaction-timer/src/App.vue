<template>
  <h1> Ninja Reaction Timer</h1>
  <button @click="start">Click to play!</button>
</template>

<script>


export default {
  name: 'App',
  components: {},
  data() {
    return {
      isPlaying: false,
      delay: null
    }
  },
  methods: {
    start() {
      this.isPlaying = true
      console.log(this.isPlaying)
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #444;
  margin-top: 60px;
}
</style>
