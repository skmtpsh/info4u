<template>
  <div class="container">
    <nav class="nav">
      <header class="Header_container">
        <div class="Header_nav_lf">
          <a href="#">Info4u</a>
          <nuxt-link :to="{name: 'MobilePage'}">about</nuxt-link>
        </div>
        <div class="Header_nav_rt"></div>
      </header>
    </nav>
    <div class="nav__placeholder"></div>
    <div class="home_ad"></div>
    <div class="home_timeline">
      <el-calendar v-model="value"></el-calendar>
      <!-- <no-ssr><el-calendar v-model="value"></el-calendar></no-ssr> -->
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      value: new Date()
    }
  },
  beforeMount () {
    // this.$router.redirect({path: 'mobile'})
  },
  methods: {
    load () {
      // this.count += 2
    }
  }
}
</script>

<style>
.container {
}
.nav__placeholder {
  height: 58px;
}
.nav {
  position: fixed;
  width: 100%;
  left: 0;
  top: 0;
  background-color: #1369bf;
  color: #fff;
  z-index: 999;
}
</style>
