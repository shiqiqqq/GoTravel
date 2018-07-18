<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl"/>
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
  export default {
    name: 'HomeSwiper',
    data(){
      return{
        swiperOption: {
          pagination: '.swiper-pagination',
          loop: true
        },
        swiperList: [{
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1806/f5/ea83238744f31102.jpg_750x200_73b8477c.jpg'
        },{
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1807/c8/2948642fbc3b6802.jpg_750x200_1fc3179f.jpg'
        }]
      }
    }
  }
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #ffffff
  .wrapper
    overflow : hidden
    width: 100%
    height: 0
    padding-bottom: 31.25%
    .swiper-img
      width:100%
</style>
