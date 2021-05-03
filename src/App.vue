<template>
  <h1>Reaction Timer</h1>
  <h2>Are you fast enough?</h2>
  <button @click="start" :disabled="isPlaying">Play</button>

  <Block v-if="delay" :delay="delay"/>
</template>

<script>
import Block from './components/Block.vue';
import Results from './components/Results.vue';

export default {
  name: 'App',
  data() {
    return {
      isPlaying: false,
      delay: null
    }
  },
  methods: {
    start() {
      this.delay = 2000 + Math.random() * 5000;
      this.isPlaying = true;
    }
  },
  components: {
    Block,
    Results
  },
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
