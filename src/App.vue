<template>
  <h2>Reaction Timer</h2>
  <button @click="startGame" :disabled="isPlaying">Play</button>

  <Block v-if="isPlaying" :delay="delay" />
</template>

<script>
import Block from "./components/Block.vue";
export default {
  name: "App",
  components: {
    Block,
  },
  data() {
    return {
      delay: null,
      isPlaying: false,
    };
  },
  methods: {
    startGame() {
      this.isPlaying = true;
      this.delay = 2000 + Math.random() * 5000;
    },
  },
};
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
