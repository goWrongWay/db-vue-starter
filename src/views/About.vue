<template>
  <div class="about">
    <h1>Test Hallo About, 这里添加的todo列表会在首页显示总数量，就是通过vuex来实现的跨组件通信</h1>
    <p>场景是某个页面或组件定义的状态需要在其他组件中使用</p>
    <p>刷新页面后状态清空</p>
    <p>如果有携带状态的需求，可以通过url带参数的形式</p>
    <SimpleTodo></SimpleTodo>
  </div>
</template>
<script>
  import SimpleTodo from '../components/SimpleTodo'
  export default {
    components: {
      SimpleTodo
    }
  }
</script>
