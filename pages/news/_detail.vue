<template>
  <div>
    <h2>News-Content :{{$route.params.detail}}</h2>
    <ul>
      <li><a href="/">Home</a></li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: "_detail",
    validate({params}) {
      // Must be a number
      return /^\d+$/.test(params.detail)
    },
    data() {
      return {
        title:this.$route.params.title,
      }
    },
    head() {
        return{
          title:this.title,
          meta:[
            {hid:'description',name:'news',content:'This is news page'}
          ]
        }
    }
  }
</script>

<style scoped>

</style>
