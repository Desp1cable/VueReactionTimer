<template>
  <h2>Reaction Time is:  {{ score }} ms</h2>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ['score'],
  data() {
    return {
      rank: null
    }
  },
  mounted() {
    if(this.score < 250){
      this.rank = 'Ultra Fust!'
    } else if (this.score < 450){
      this.rank = 'Pretty Fust'
    } else {
      this.rank = 'Could Be Better'
    }
  }
}
</script>

<style>
.rank {
  font-size: 1.4em;
  color: #0faf87;
  font-weight: bold;
}
</style>