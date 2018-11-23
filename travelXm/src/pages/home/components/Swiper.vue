<template>
  <div class="wrapper">
    <swiper :options="swiperOption" >
      <swiper-slide v-for="item in swiperList" :key="item.id"><img class="swiper-img" :src="item.imgUrl"></swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: require('./pic/1.jpg')
      },{
        id: '0002',
        imgUrl: require('./pic/2.jpg')
      },{
        id: '0003',
        imgUrl: require('./pic/3.jpg')
      },{
        id: '0004',
        imgUrl: require('./pic/4.jpg')
      },{
        id: '0005',
        imgUrl: require('./pic/5.jpg')
      },{
        id: '0006',
        imgUrl: require('./pic/6.jpg')
      },{
        id: '0007',
        imgUrl: require('./pic/7.jpg')
      },{
        id: '0008',
        imgUrl: require('./pic/8.jpg')
      },{
        id: '0009',
        imgUrl: require('./pic/9.jpg')
      },{
        id: '00010',
        imgUrl: require('./pic/10.jpg')
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 26%
    background: #eee
    .swiper-img
      width: 100%
</style>
