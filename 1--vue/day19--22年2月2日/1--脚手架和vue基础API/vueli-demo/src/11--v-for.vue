<template>
  <div id="app">
    <!-- vue最常用指令, 铺设页面利器, 快速把数据赋予到相同的dom结构上循环生成 -->
    <!-- v-for="(值,索引) in 目标结构" -->
    <!-- v-for="值 in 目标结构" -->

    <div>
      <p>学生姓名</p>
      <ul>
        <li v-for="(item, index) in arr" :key="item">
          {{ index }} - {{ item }}
        </li>
      </ul>
      
      <p>学生详细信息</p>
      <ul>
        <li v-for="obj in stuArr" :key="obj.id">
          <span>{{ obj.name}}</span>
          <span>{{ obj.sex}}</span>
          <span>{{ obj.hobby}}</span>
        </li>
      </ul>
      <!-- v-for 遍历对象（了解） -->
      <p>老师信息</p>
      <div v-for="(value, key) in tObj" :key="value">
        {{ key }} -- {{ value }}
      </div>

      <!-- v-for 遍历整数（了解）从1开始 -->
      <div v-for="i in count" :key="i">{{ i }}</div>
    </div>

  </div>
</template>

<script>
export default {
  data() {
    return {
      arr:["小明","小欢欢","大黄"],
      stuArr: [
        {
          id: 1001,
          name: "孙悟空",
          sex: "男",
          hobby: "吃桃子",
        },
        {
          id: 1001,
          name: "孙悟空",
          sex: "男",
          hobby: "吃桃子",
        },
      ],
      tObj: {
        name: "小黑",
        age: 18,
        class: "1期",
      },
      count: 10,
    }
  },
}
</script>

<style>

</style>