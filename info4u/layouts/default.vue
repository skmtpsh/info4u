<template>
  <div id="app">
    <nav class="nav">
      <header class="Header_container">
        <div class="Header_nav_lf">
          <a href="#"><b style="font-size:18px;">某刻</b></a>
        </div>
        <div class="Header_nav_lf">
          <nuxt-link :to="{path: '/', params: {}}">首页</nuxt-link>
          <!-- <nuxt-link :to="{path: '/mobile', params: {}}">mobile</nuxt-link> -->
          <nuxt-link :to="{path: '/movie', params: {}}">影院</nuxt-link>
          <nuxt-link :to="{path: '/story', params: {}}">书城</nuxt-link>
          <nuxt-link :to="{path: '/news', params: {}}">发现</nuxt-link>
        </div>
        <div class="Header_nav_rt">
          <el-button round size="small"><i class="el-icon-user"></i> 登录/注册</el-button>
        </div>
      </header>
    </nav>
    <div class="nav__placeholder"></div>
    <div class="banner-ad">
      <!-- <img :src="require('@/assets/img/ad.png')" /> -->
    </div>
    <nuxt />
    <div id="footer">
      <!-- <p><a href="#">关于我们</a></p> -->
      互联网违法和不良信息投诉：01061840600-8030 / 违法(含侵权)及不良信息投诉指引 © 2019 版权所有
    </div>
  </div>
</template>
<script>
export default {
  name: 'LayOutPage',
  data() {
    return {
      list: []
    }
  }
}
</script>