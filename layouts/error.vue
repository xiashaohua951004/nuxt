<template>
  <div>
    <h2 v-if="error.statusCode==404">bucunzai</h2>
    <h2 v-else>500</h2>
    <nuxt-link :to="{name:'index'}">HOME</nuxt-link>
  </div>
</template>

<script>
  export default {
    name: "error",
    props: ['error'],
    head() {
      return{
        title:404
      }
    }
  }
</script>

<style scoped>

</style>
