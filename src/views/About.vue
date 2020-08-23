<template>
  <div class="about">
    <h1>This is an about page</h1>
    <button @click="handleRouter">传参跳转home</button>
  </div>
</template>

<script>
export default {
  methods:{
    handleRouter(){
      this.$router.push({
        name:'Home',
        query:{
          id:1,
          num:2
        }
      })
    }
  },
  mounted(){
    console.log(this.$route)
  }
}
</script>

<style>

</style>
