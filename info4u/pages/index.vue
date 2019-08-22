<template>
  <div class="container">
    <div class="home_ad"></div>
    <div class="home_timeline">
      <!-- <no-ssr><el-calendar v-model="value"></el-calendar></no-ssr> -->
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
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

</style>
