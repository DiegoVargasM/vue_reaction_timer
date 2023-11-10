<template>
  <p>Reaction Time: {{ score }} ms</p>
  <p class="rank">Rank: {{ rank }}</p>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score < 250) {
      this.rank = "Ninja Fingers!";
    } else if (this.score < 400) {
      this.rank = "Average Joe.";
    } else {
      this.rank = "Snail peaced...";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.5rem;
  font-weight: bold;
  color: #f00;
}
</style>
