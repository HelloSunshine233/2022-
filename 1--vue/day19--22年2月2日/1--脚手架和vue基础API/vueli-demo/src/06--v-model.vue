<template>
  <div>
    <!--v-model="vue数据变量"  -->
    <!-- 目标就是把value属性和vue数据变量，双向绑定到一起 -->
    
     <!-- 1 -->
     <div>
        <!-- v-model:是实现vue.js变量和表单标签value属性，双向绑定的指令 -->
        <!-- 表单元素指的是不同类型的input元素,复选框，单选按钮，提交按钮 -->

        <!-- input 后面的type类型可以选择好多的形态：text,radio,submit,password,checkbox, -->
        <!-- 1 文本域 -->
        <div>
          <span>用户名:</span>
          <input type="text" v-model="username" />
        </div>
        <!-- 1.2 密码字段 -->
        <div>
          <span>密码:</span>
          <input type="password" v-model="pass">
        </div>
        <!-- 2 复选框-->
        <div>
          <span>来自于:</span>
          <!-- 下拉菜单要绑定在select上 -->
          <!-- <select v-model="from"> -->
          <select v-model="from">
            <!-- value 这个属性的值表示被选中时提交给表单的值，如果省略了这个属性的值，值就从选项元素的文本内容中获取 -->
            <option value="北京市">北京</option>
            <option value="南京市">南京</option>
            <option value="天津市">天津</option>
          </select>
        </div>
        <!-- 3 多选按钮 -->
        <div>
          <span>爱好:</span>
          <input type="checkbox" v-model="hobby" value="抽烟">抽烟
          <input type="checkbox" v-model="hobby" value="喝酒">喝酒
          <input type="checkbox" v-model="hobby" value="写代码">写代码
        </div>
        <!-- 4 单选按钮 -->
        <div>
          <span>性别:</span>
          <!-- 使用 name 属性定义的单选按钮组 (具有相同名称的单选按钮 属于同一组)。
          name 属性用于表单提交后向服务器传送数据，或者在Javascript引用表单数据。
          注意： 在表单提交后只有表单元素的 name 属性才会传递数据值。 -->
          <input type="radio" value="男" name="sex" v-model="gender">男
          <input type="radio" value="女" name="sex" v-model="gender">女
        </div>
        <!-- 5 文本域 -->
        <div>
          <span>自我介绍</span>
          <textarea v-model="intro"></textarea>
        </div>
       
     </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username:"",
      pass:"",
      from:"",
      hobby:[],
      gender:"",
      intro:"",
    }
  },
}
</script>

<style>

</style>