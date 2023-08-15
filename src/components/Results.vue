<template>
  <p>Reaction Time:{{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
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
      this.rank = "you are excellent";
    } else if (this.score < 400) {
      this.rank = "you are good";
    } else {
      this.rank = "not bad";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4em;
  color: #0faf78;
  font-weight: bold;
}
</style>
