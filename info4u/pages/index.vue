<template>
  <div class="container">
    <el-row :gutter="40">
      <el-col :span="16">
        <el-tabs v-model="activeName" @tab-click="handleClick">
          <el-tab-pane label="推荐" name="first">
            <ul>
              <li v-for="(i, index) in count" :key="index" class="item_list" >
                <h3><a href="#">天邦-天风2019.8.21电话会不完整记录</a></h3>
                <p>半年报解读，生产性生物资产、消耗性生物资产解读： 董秘承认半年报经营状况不理想，一季度亏损3亿，二季度亏损约6000万。非洲猪瘟疫情超预期，防疫工作主要放在了母猪场，家庭农场的防疫工作做的不到位。 对于原先对外表示二季度较一季度能繁母猪有所回升的表述向投资者道...</p>
                <div class="item_line">
                  <div class="item_lb">
                    <span>胖子</span><span>08-21 23:51</span>
                  </div>
                  <div class="item_rt">
                    2.1万人阅读
                  </div>
                </div>
              </li>
            </ul>
            <!-- <h3>本期主打</h3> -->
            <ul class="aui-book-list">
              <li class="aui-flex">
                <div class="aui-book-img">
                  <img :src="require('@/assets/img/book1.png')" />
                </div>
                <div class="aui-flex-box">
                  <h2>文化苦旅 <em>9.9分</em></h2>
                  <p>《文化苦旅》是于秋生的第一个散文集所有的作品主要包括了俩部分一部分是历史文学</p>
                  <h3><i>于秋生著</i> <em>加入书架</em></h3>
                </div>
              </li>
              <li class="aui-flex">
                <div class="aui-book-img">
                  <img :src="require('@/assets/img/book2.png')" />
                </div>
                <div class="aui-flex-box">
                  <h2>我在云上爱你 <em>9.9分</em></h2>
                  <p>《文化苦旅》是于秋生的第一个散文集所有的作品主要包括了俩部分一部分是历史文学</p>
                  <h3><i>于秋生著</i> <em>加入书架</em></h3>
                </div>
              </li>
              <li class="aui-flex">
                <div class="aui-book-img">
                  <img :src="require('@/assets/img/book3.png')" />
                </div>
                <div class="aui-flex-box">
                  <h2>我在云上爱你 <em>9.9分</em></h2>
                  <p>《文化苦旅》是于秋生的第一个散文集所有的作品主要包括了俩部分一部分是历史文学</p>
                  <h3><i>于秋生著</i> <em>加入书架</em></h3>
                </div>
              </li>
              <li class="aui-flex">
                <div class="aui-book-img">
                  <img :src="require('@/assets/img/book4.png')" />
                </div>
                <div class="aui-flex-box">
                  <h2>我在云上爱你 <em>9.9分</em></h2>
                  <p>《文化苦旅》是于秋生的第一个散文集所有的作品主要包括了俩部分一部分是历史文学</p>
                  <h3><i>于秋生著</i> <em>加入书架</em></h3>
                </div>
              </li>
            </ul>
          </el-tab-pane>
          <el-tab-pane label="今日" name="second">配置管理</el-tab-pane>
          <el-tab-pane label="排行" name="third">角色管理</el-tab-pane>
          <el-tab-pane label="24小时" name="fourth">定时任务补偿</el-tab-pane>
        </el-tabs>
      </el-col>
      <el-col :span="8">
        <div class="advise">
          <img :src="require('@/assets/img/bn3.jpg')" />
        </div>
        <ul class="home_list">
          <li>
            <a href="#" target="_blank">
              <i><svg-icon icon-class="movie" /></i>
              <strong>蛋卷基金</strong>
              <span>万2.5低佣<i class="iconfont"></i></span>
               <em><svg-icon icon-class="arr" /></em>
            </a>
          </li>
          <li>
            <a href="#" target="_blank">
              <i><svg-icon icon-class="story" /></i>
              <strong>A股开户</strong><span>万2.5低佣<i class="iconfont"></i></span>
               <em><svg-icon icon-class="arr" /></em>
            </a>
          </li>
          <li>
            <a href="#" target="_blank">
              <i><svg-icon icon-class="news" /></i>
              <strong>蛋卷基金</strong><span>万2.5低佣<i class="iconfont"></i></span>
               <em><svg-icon icon-class="arr" /></em>
            </a>
          </li>
        </ul>
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
  name: 'HomePage',
  data() {
    return {
      count: 5,
      activeName: 'first'
    }
  },
  head() {
    return {
      title: '首页'
    }
  },
  beforeMount () {
    // this.$router.redirect({path: 'mobile'})
  },
  methods: {
    handleClick(tab, event) {
      // console.log(tab, event);
    },
    load () {
      // this.count += 2
    }
  }
}
</script>

<style>

</style>
