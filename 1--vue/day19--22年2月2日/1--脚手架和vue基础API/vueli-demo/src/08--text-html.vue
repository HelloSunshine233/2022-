<template>
  <div>
    <!-- v-text把值当成普通字符串显示, v-html把值当做html解析 -->
    <p v-text="str"></p>
    <p v-html="str"></p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      str:"<span>Nihao丶少年</span>"
    }
  },
}
</script>

<style>

</style>