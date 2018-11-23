<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl"/>
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconList: [{
        id: '0001',
        imgUrl: require('./pic/jingdian.png'),
        desc: '景点门票'
      },{
        id: '0002',
        imgUrl: require('./pic/yiri.png'),
        desc: '一日游'
      },{
        id: '0003',
        imgUrl: require('./pic/biyou.png'),
        desc: '上海比游'
      },{
        id: '0004',
        imgUrl: require('./pic/haichang.png'),
        desc: '上海海昌'
      },{
        id: '0005',
        imgUrl: require('./pic/wenquan.png'),
        desc: '泡温泉'
      },{
        id: '0006',
        imgUrl: require('./pic/shengdi.png'),
        desc: '打卡圣地'
      },{
        id: '0007',
        imgUrl: require('./pic/huanle.png'),
        desc: '上海欢乐谷'
      },{
        id: '0008',
        imgUrl: require('./pic/dong.png'),
        desc: '野生动物园'
      },{
        id: '0009',
        imgUrl: require('./pic/dishini.png'),
        desc: '上海迪士尼'
      },{
        id: '00010',
        imgUrl: require('./pic/quan.png'),
        desc: '全部玩乐'
      }]
    }
  },
  computed: {
    pages() {
      const pages = []  // 定义一个空的一维数组
      this.iconList.forEach((item,index) => {
        const page = Math.floor(index / 8)  // 只有0/1两个值
        if(!pages[page]) {  /* 如果 不存在，就在下面添加一个数组，变成了二维数组*/
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  @import "~styles/mixins.styl"
  .icons >>> .swiper-container
    height: 0
    padding-bottom: 50%
  .icon
    overflow: hidden
    position: relative
    float: left
    width: 25%
    height: 0
    padding-bottom: 25%
    .icon-img
      position: absolute
      top: 0
      left: 0
      right: 0
      bottom: .44rem
      box-sizing: border-box
      padding: .1rem
      .icon-img-content
        display: block
        margin: 0 auto
        height: 100%
    .icon-desc
      position: absolute
      left: 0
      right: 0
      bottom: 0
      height: .44rem
      line-height: .44rem
      text-align: center
      color: $darkTextColor
      ellipsis()
</style>
