<template>
  <div>
    <ul>
      <li v-for="(item,ind) in arr" :key="ind">
        <span>{{ item }}</span>
        <!-- 这个地方需要传递参数 -->
        <button @click="del(index)">删除</button>
      </li>
    </ul>
    <button @click="add">生成</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr:[1, 3, 4]
    }
  },
  methods: {
    del(index) {
      
      this.arr.splice(index, 1)
    },
    add() {
      // Math.floor() 返回小于或等于一个给定数字的最大整数。
      this.arr.push(Math.floor(Math.random() * 20))
    }
  }
}
</script>

<style>

</style>