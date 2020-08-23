<template>
  <div class="home">
    <button @click="handleRoute">路由传参测试到about</button>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  mounted(){
    console.log(this.$route)
  },
  methods:{
    handleRoute(){
      this.$router.push({
        name:'About',
        query:{
          id:'test',
          num:22,
          page:333,
          index:44,
          text:"文字"
        }
      })
    }
  }
}
</script>
