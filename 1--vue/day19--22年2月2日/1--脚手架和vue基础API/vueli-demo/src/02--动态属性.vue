<template>
  <div>


    <p>你要买的商品数量：{{ count }}</p>
    <button @click="count = count + 1">增加1</button>
    <button @click="addFn">增加1</button>
    <button v-on:click="addCountFn(5)">一次增加5件</button>

    <button @click="subFn">减少</button>  
  </div>
  
  
  

</template>

<script>
  export default{
    data() {
      return {        
          count: 3
        }
    },
    // methods，少加了一个s,为什么会影响这么大呢
    methods: {
      addFn() {
        this.count++
      },
      addCountFn(num) {
        this.count += num
      },
      subFn() {
        this.count--
      }
    },
  }
  

</script>

<style>

</style>
