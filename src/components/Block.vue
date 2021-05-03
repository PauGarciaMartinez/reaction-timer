<!-- TEMPLATE -->
<template>
  <div class="block" v-if="showBlock">Click Me</div>
</template>

<!-- SCRIPT -->
<script>
export default {
  name: 'Block',
  props: ['delay'],
  data() {
    return {
      showBlock: false
    }
  },
  mounted() {
    setTimeOut(() => { this.showBlock = true }, this.delay);
  },
  update() {

  }
}
</script>

<!-- STYLE -->
<style>
  .block {
    width: 400px;
    border-radius: 20px;
    background: #0faf87;
    color: white;
    text-align: center;
    padding: 100px 0;
    margin: 40px auto;
  }
</style>