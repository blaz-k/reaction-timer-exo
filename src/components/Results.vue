<template>
  <div>
    <p>Score is: {{ score }} ms</p>
    <p class="rank">{{ rank }}</p>
  </div>
</template>

<script>
export default {
  name: "Results",
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score < 280) {
      this.rank = "You are a click ninja 🥷🏻";
    } else if (this.score < 450) {
      this.rank = "Rapid reflexes 🐇";
    } else {
      this.rank = "Not something to talk about in job 🥱 🐌";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.5rem;
  color: aquamarine;
  font-weight: bold;
}
</style>
