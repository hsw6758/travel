<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img :src="item.imgUrl" class="item-img">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'HomeWeekend',
    data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: require('./pic/wk1.jpg'),
        title: '上海去哪儿泡温泉',
        desc: '上海的朋友总会问，哪里可以泡温泉，哪里的温泉好呢'
      },{
        id: '0002',
        imgUrl: require('./pic/wk2.jpg'),
        title: '上海赏秋攻略',
        desc: '上海的秋天，哪里都是美美哒'
      },{
        id: '0003',
        imgUrl: require('./pic/wk3.jpg'),
        title: '上海必游TOP10',
        desc: '中西合璧，现代和传统各有各的精彩'
      },{
        id: '0004',
        imgUrl: require('./pic/wk4.jpg'),
        title: '亲子时光TOP榜',
        desc: '走进自然或玩转乐园，感知大千世界'
      }]
    }
  }
  }
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 37.09%
    .item-img
      width: 100%
  .item-info
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #616161
      ellipsis()
</style>
