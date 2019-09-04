<template>
  <div class="container">
    <el-row :gutter="40">
      <el-col :span="16">
        分支
        <h2>{{detail.title}}</h2>
        <p>{{detail.summary}}</p>
        <p><el-tag v-for="tag in detail.tags" :key="tag">{{tag}}</el-tag></p>
      </el-col>
    </el-row>
  </div>
</template>
<script>
  export default {
    // validate({ params, query }) {
    //   return /^(?![0-9]+$)(?![a-zA-Z]+$)[0-9A-Za-z]+$/.test(params.id) // must be number
    // },
    async asyncData (context) {
      const { app, params } = context
      const res = await app.$axios.get(`/api/movie/subject/${params.id}?apikey=0df993c66c0c636e29ecbb5344252a4a`);
      return {
        detail: res.data
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