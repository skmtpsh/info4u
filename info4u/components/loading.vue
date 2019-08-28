<template lang="html">
  <div v-if="loading" class="loading-page">
    <i class="el-icon-loading"></i>
  </div>
</template>

<script>
export default {
  data: () => ({
    loading: false
  }),
  methods: {
    start () {
      this.loading = true
    },
    finish () {
      setTimeout(() => {
        this.loading = false
      }, 1000)
    }
  }
}
</script>