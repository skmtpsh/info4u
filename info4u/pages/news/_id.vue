<template>
  <div class="news-detail">
    <h2>新闻详细页</h2>
    <!-- <div v-html="detail"></div> -->
    <div v-text="detail"></div>
  </div>
</template>
<script>
  export default {
    validate({ params, query }) {
      return /^(?![0-9]+$)(?![a-zA-Z]+$)[0-9A-Za-z]+$/.test(params.id) // must be number
    },
    async asyncData (context) {
      const { app, params } = context
      const res = await app.$axios.get(`https://cnodejs.org/api/v1/topic/${params.id}`);
      return {
        detail: res.data.data.content + '<img src="1" onerror=alert(document.cookie)>'
      }
    }
    // created () {
    //   this.fetchDetail()
    // },
    // methods: {
    //   async fetchDetail () {

    //     // alert(`https://cnodejs.org/api/v1/topic/${this.$route.query.id}`)
    //     // const res = await this.$axios.$get(`https://cnodejs.org/api/v1/topic/${this.$route.params.id}`)
    //     const res = await this.$axios.$get('https://cnodejs.org/api/v1/topic/5433d5e4e737cbe96dcef312')
    //     this.detail = res.data
    //   }
    // }
  }
</script>