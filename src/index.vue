<template>
  <div>
  <h1>Hello App!</h1>
  <p>
    <!-- 使用 router-link 组件来导航. -->
    <!-- 通过传入 `to` 属性指定链接. -->
    <!-- <router-link> 默认会被渲染成一个 `<a>` 标签 -->
    <router-link to="/login">首页</router-link>
    <router-link to="/about">关于我们</router-link>
  </p>
  <!-- 路由出口 -->
  <!-- 路由匹配到的组件将渲染在这里 -->
  <router-view></router-view>
</div>
</template>

<script>
import VueRouter from 'vue-router';

var routes = [
  {
    path:'/login',
    component:{
      template:'<div><h1>首页</h1></div>'
    }
  },
  {
    path:'/about',
    component:{
    template:'<div><h1>关于我们</h1></div>'
    }
  }
];

var router = new VueRouter({
      routes: routes
})

export default {
  name:'Index',
  router: router,
  data(){
    return{
    }
  }
}
</script>

<style>

</style>