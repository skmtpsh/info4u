<template>
  <div class="news">
    <h2>小说列表</h2>
    <ul>
      <nuxt-link v-for="(item, index) in list" :key="index" :to="'/story/' + item.id" tag="li" ><a>{{item.title}}</a></nuxt-link>
    </ul>
    <!-- <nuxt-link :to="{path: '/'}">首页</nuxt-link> -->
  </div>
</template>

<script>
export default {
  name: 'StoryPage',
  data() {
    return {
      list: []
    }
  },
  head() {
    return {
      title: '爱看小说'
    }
  },
  middleware: 'userAuth',
  // transition(to, from) {
  //   if (to.name === 'news') {
  //     // 设置动画名称
  //     return 'slide-left'
  //   } else {
  //     return 'slide-right'
  //   }
  // },
  async asyncData({ $axios }) {
    // this.list = await $axios.$get('https://cnodejs.org/api/v1/topics')
  },
  created () {
    this.fetchList()
  },
  methods: {
    async fetchList () {
      const res = await this.$axios.$get('https://cnodejs.org/api/v1/topics')
      this.list = res.data
    }
  }
}
</script>
