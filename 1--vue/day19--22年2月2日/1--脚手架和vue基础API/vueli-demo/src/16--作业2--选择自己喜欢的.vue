<template>
  <div>
    <div>选择自己喜欢的</div>
    <!-- 行内块元素 -->
      <div v-for="(str, index) in arr" :key="index" style="display:inline-block;">
      <!-- <div v-for="(str, index) in arr" :key="index"> -->
        <input type="checkbox" v-model="checkArr" :value="str"/>
        <!-- <input type="checkbox" v-model="checkArr"/> -->
        <span>{{ str }}</span>
      </div>
    <!-- 2. 选择了就显示出来，用的v-model这个真的想不懂 -->
    <ul >
      <li v-for="(item,index) in checkArr" :key="index">
        {{ item }}
      </li>
    </ul>
  </div>
</template>

  <!-- 
    1. v-model的作用是什么 数据双向绑定
    v-model其实是个语法糖，它实际上是做了两步动作：
    1、绑定数据value
    2、触发输入事件input
    绑定数据并且监听数据改变，v-model可以在input和textarea，select上面进行双向数据绑定
  -->
  <!-- 
    （2）这里的value又是什么作用呢？
  -->

<script>
export default {
  data() {
    return {
      arr:["科幻", "喜剧", "动漫", "冒险", "科技", "军事", "娱乐", "奇闻"],
      checkArr: [] // 收集选中的复选框的value值
    }
  },
}
</script>

<style>

</style>