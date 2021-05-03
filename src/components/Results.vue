<!-- TEMPLATE -->
<template>
  <p>Your score is {{ score }}ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<!-- SCRIPT -->
<script>
export default {
  name: 'Results',
  props: ['score'],
  data() {
    return {
      rank: null
    }
  },
  mounted() {
    if (this.score < 250) this.rank = 'Ninja Fingers';
    else if (this.score < 400) this.rank = 'Rapid Reflexes';
    else this.rank = 'Snail pace...';
  }
}
</script>

<!-- STYLE -->
<style>
.rank {
  font-size: 1.4rem;
  color: #0faf87;
  font-weight: 800;
}
</style>