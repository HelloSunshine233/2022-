<template>
  <div>
    <ul>
      <!-- <li>帅哥</li>
      <li>美女</li>
      <li>程序猿</li> -->
      <li v-for="(item,index) in arr" :key="index">
        {{ item }}
      </li>
    </ul>
    <!-- 还是有点不知道怎么处理这里的点击事件 -->
    <button @click="btn">走一走</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr: ["帅哥","美女","程序猿"],
    }
  },
  methods: {
    btn() {
      // 把头部的数据加入到末尾
      this.arr.push(this.arr[0]);
      // 再把头部的数据给删除掉
      this.arr.shift();
    }
  },
}
</script>

<style>

</style>