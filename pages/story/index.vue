<template>
  <div class="container">
    <el-row :gutter="40">
      <el-col :span="16">
        <h2>书架列表</h2>
        <ul class="aui-book-list">
          <nuxt-link v-for="(item, index) in list" :key="index" :to="'/movie/' + item.id" tag="li" class="aui-flex">
            <div class="aui-book-img">
              <img :src="require('@/assets/img/book1.png')" />
            </div>
            <div class="aui-flex-box">
              <h2>文化苦旅 <em>9.9分</em></h2>
              <p>{{item.title}}</p>
              <h3><i>于秋生著</i> <em>立即阅读</em></h3>
            </div>
          </nuxt-link>
        </ul>
      </el-col>
      <el-col :span="8">
        <div class="advise">
          <img :src="require('@/assets/img/bn3.jpg')" />
        </div>
        <div class="mod2">
          <h3>今日更新</h3>
          <ul class="mod_list">
            <li>
                <a href="#" target="_blank">
                  <i>1</i>
                  <strong>蛋卷基金</strong>
                  <span>万2.5低佣<i class="iconfont"></i></span>
                </a>
              </li>
              <li>
                <a href="#" target="_blank">
                  <i>2</i>
                  <strong>A股开户</strong><span>万2.5低佣<i class="iconfont"></i></span>
                </a>
              </li>
              <li>
                <a href="#" target="_blank">
                  <i>3</i>
                  <strong>蛋卷基金</strong><span>万2.5低佣<i class="iconfont"></i></span>
                </a>
              </li>
          </ul>
        </div>
        <div class="mod">
          <h3>热门排行</h3>
          <ul>
            <li><a href="#" target="_blank">中国金茂：获准发行20亿元公司债券 票面利率3.65%</a></li>
            <li><a href="#" target="_blank">Costco大陆首店开业，卖16万张会员卡，美方管理人员笑了</a></li>
            <li><a href="#" target="_blank">结账2小时、中途暂停营业，上海Costco开业首日的体验很崩溃</a></li>
            <li><a href="#" target="_blank">《美国工厂》火了！奥巴马为什么盯上了曹德旺？</a></li>
            <li><a href="#" target="_blank">因长沙市一小区业主业主反对建基站 三大运营商将断电拆除</a></li>
            <li><a href="#" target="_blank">Costco上海被挤爆！会员卡卖出16万张，玩了43年“新零售”，它是如何做到的？</a></li>
            <li><a href="#" target="_blank">以色列空袭邻国，中东三国誓言报复</a></li>
            <li><a href="#" target="_blank">Costco刷屏中国！上午开业下午停业：10万爱马仕秒光，更别提茅台、五粮液</a></li>
          </ul>
        </div>
        <div class="mod">
          <h3>最新新闻</h3>
          <ul>
            <li><a href="#" target="_blank">中国金茂：获准发行20亿元公司债券 票面利率3.65%</a></li>
            <li><a href="#" target="_blank">Costco大陆首店开业，卖16万张会员卡，美方管理人员笑了</a></li>
            <li><a href="#" target="_blank">结账2小时、中途暂停营业，上海Costco开业首日的体验很崩溃</a></li>
            <li><a href="#" target="_blank">《美国工厂》火了！奥巴马为什么盯上了曹德旺？</a></li>
            <li><a href="#" target="_blank">因长沙市一小区业主业主反对建基站 三大运营商将断电拆除</a></li>
            <li><a href="#" target="_blank">Costco上海被挤爆！会员卡卖出16万张，玩了43年“新零售”，它是如何做到的？</a></li>
            <li><a href="#" target="_blank">以色列空袭邻国，中东三国誓言报复</a></li>
            <li><a href="#" target="_blank">Costco刷屏中国！上午开业下午停业：10万爱马仕秒光，更别提茅台、五粮液</a></li>
          </ul>
        </div>
      </el-col>
    </el-row>
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
