<template>
  <div>
    <ul>
      <li v-for="(val, index) in arr" :key="index">
        {{ val }}
      </li>
    </ul>
    <!--  -->
    <button @click="revBtn">数组翻转</button>
    <button @click="sliceBtn">截取前3个</button>
    <button @click="updateBtn">更新第一个元素值</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr: [5, 3, 9, 2, 1]
    }
  },
  methods: {
    revBtn() {
      // 1. 数组翻转可以让v-for更新
      this.arr.reverse()
    },
    sliceBtn() {
      // 2. 数组slice方法不会造成v-for 更新

    }
  },
}
</script>

<style>

</style>