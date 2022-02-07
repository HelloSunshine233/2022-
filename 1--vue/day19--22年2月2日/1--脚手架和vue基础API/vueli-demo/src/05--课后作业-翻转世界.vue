<template>
  <div>
   <h1>{{ message }}</h1>
    <button @click="btn">逆转世界</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: "Hello World"
    }

  },
  methods: {
    // 这和个地方，有点忘记了
    btn() {
      // split() 方法用于把一个字符串分割成字符串数组。
      // reverse() 颠倒数组中元素的顺序：
      // join() 把数组中的所有元素转换为一个字符串：
      this.message = this.message.split("").reverse().join("")
    }
  },
};
</script>

<style>

</style>