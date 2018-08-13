<template>
  <div>
    <ul>
      <li><nuxt-link :to="{name:'index'}">HOME</nuxt-link></li>
      <li><nuxt-link :to="{name:'about-list'}">ABOUT</nuxt-link></li>
      <li><nuxt-link :to="{name:'news-list',params:{id:123, newsId:3306}}">NEWS</nuxt-link></li>
      <li><nuxt-link :to="{name:'news-list',params:{id:222, newsId:555}}">NEWS</nuxt-link></li>
      <li><nuxt-link :to="{name:'news-detail',params:{detail:555,title:'绍华'}}">NEWSdetail</nuxt-link></li>
      <li><nuxt-link :to="{name:'acticty-ansyData',params:{ansyData:77,title:'新闻一'}}">活动</nuxt-link></li>
      <li><nuxt-link :to="{name:'acticty-ansyData',params:{ansyData:78,title:'新闻二'}}">会议</nuxt-link></li>
    </ul>
  </div>
</template>

<script>

export default {
  components: {
  }
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>

