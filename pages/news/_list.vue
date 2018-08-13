<template>
  <div>
    <h2>News Index page</h2>
    <p>newsId:{{newsId}}</p>
    <ul>
      <li><a href="/">Home</a></li>
      <li><nuxt-link :to="{name:'news-detail',params:{detail:123,title:'sha'}}">News-1</nuxt-link></li>
      <li><nuxt-link :to="{name:'news-detail',params:{detail:456}}">News-2</nuxt-link></li>
    </ul>
  </div>
</template>

<script>
    export default {
        name: "index",
      data(){
          return{
            newsId:this.$route.params.newsId
          }
      }
    }
</script>

<style scoped>

</style>
