<template>
  <div>
    <!-- 用v-bind 给标签class设置动态的值 -->
    <!-- vue变量控制标签是否应该有类名 -->
    <p :class="{red_str: bool}">动态的class</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      bool: true
    }
  },
}
</script>

<style>
  .red_str {
    color: red;
  }
</style>