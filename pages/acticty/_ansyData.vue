<template>
  <div>
    <h1>姓名：{{data.message}}</h1>
    <h2>年龄：{{data.data}}</h2>
    <h2 ref="sdf">兴趣：</h2>
    <nuxt-link :to="{name:'index'}">HOME</nuxt-link>
    <p @click="clic">132</p>
  </div>
</template>

<script>
  import axios from '~/plugins/axios'

  export default {
    name: "ansyData",
    data() {
      return {
        title: this.$route.params.title,
        data: {}
      }
    },
    async asyncData({params}) {
      let {data} = await axios.get('/api/news/list?', {params: {columnId:params.ansyData}})
      console.log(data.data)
      return {data: data}
    },
    head() {
      return {
        title: this.title
      }
    },

    methods: {
      clic() {
        console.log(this.$refs.sdf.innerHTML)
      }
    }
  }
</script>

<style scoped>

</style>
