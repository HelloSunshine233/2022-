<template>
  <div>
    <span>自我介绍:</span>
    <!-- 在change时出发而非input时 -->
    <!-- 用于将 v-model 的触发方式由 input 事件触发更改为 change 事件触发 -->
    <!-- 如果我们希望将 v-model 双向数据绑定的触发方式从 ipnut 事件的每次输入就更新的这种触发方式更改为想 change 事件一样的触发方式，也就是每一次进行输入内容完毕以后，失去焦点时进行内容检测，如果新内容与旧内容不同时，再去进行双向数据绑定视图更新 -->

    <textarea v-model.lazy="intro"></textarea>
    <textarea v-model="intro1"></textarea>
  </div>
</template>

<script>
export default {
  data() {
    return {     
      intro: "",
      intro1: ""
    }
  }
}
</script>

<style>

</style>