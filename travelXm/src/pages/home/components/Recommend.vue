<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img :src="item.imgUrl" class="item-img">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: require('./pic/laxiangguan.jpg'),
        title: '上海杜莎夫人蜡像馆',
        desc: '上海杜莎夫人蜡像馆'
      },{
        id: '0002',
        imgUrl: require('./pic/huanlegu.jpg'),
        title: '上海欢乐谷',
        desc: '浪漫上上海欢乐谷，青春的气息'
      },{
        id: '0003',
        imgUrl: require('./pic/dishini.jpg'),
        title: '上海迪士尼乐园',
        desc: '浪漫上童年时光'
      },{
        id: '0004',
        imgUrl: require('./pic/shuizuguan.jpg'),
        title: '上海海洋水族馆',
        desc: '蓝色海洋，无尽的欢乐'
      },{
        id: '0005',
        imgUrl: require('./pic/dongwuyuan.jpg'),
        title: '上海动物园',
        desc: '浪漫上海黄浦江，浪漫的黄浦江夜景'
      },{
        id: '0006',
        imgUrl: require('./pic/huangpujiang.jpg'),
        title: '黄浦江夜游',
        desc: '浪漫上海黄浦江，浪漫的黄浦江夜景'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent:  .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: .44rem
        margin-top: .16rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
