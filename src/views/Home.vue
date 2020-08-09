<template>
  <div class="about">
    <h1>Test Hallo Home</h1>
    <h3>
      网页主题色通过 iview-variables.less 修改
    </h3>
    <h4>
      路由已经配好。
      <ul>
        <li>1.新增页面在views文件夹下新建</li>
        <li>2.router里面配置一下</li>
        <li>3.App.vue中设置左侧导航列表，并且在MenuItem上配置name与to属性，这样才能在任意路径下刷新页面返回正确的选中状态</li>
      </ul>

    </h4>
    <p>todo 数量{{todoCount}}</p>
  </div>
</template>
<script>
  import store from '../store';

  export default {
    data() {
      return {
        todoCount: store.state.todos.length
      }
    },

  }
</script>