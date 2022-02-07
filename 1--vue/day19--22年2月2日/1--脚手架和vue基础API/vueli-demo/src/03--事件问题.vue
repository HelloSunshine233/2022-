<template>
  <div>
    <a @click="one" href="http://www.baidu.com">阻止去百度</a>
    <hr>
    <a @click="two(10, $event)" href="http://www.taobao.com">阻止去淘宝</a>
  </div>
</template>

<script>
  export default{
    data() {
      
    },
    methods: {
      one(e) {
        e.preventDefault()
      },
      two(num, e) {
        e.preventDefault()
      }
    }
  }
  

</script>

<style>

</style>
