<template>
  <div class="wrapper">
    <swiper :options="swiperOptions">
    <swiper-slide v-for="item in swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" alt="">
    </swiper-slide>
     
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
export default {
  name : 'HomeSwiper',
  data(){
      return {
          swiperOptions:{
              pagination:'.swiper-pagination',
              loop:true
          },
          swiperList:[
              {
                  id:'0001',
                  imgUrl:'//img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_600x330_bf9c4904.jpg'
              },
              {
                  id:'0002',
                  imgUrl:'//img1.qunarzz.com/sight/p0/1807/7d/7d64de6b134d10eaa3.img.jpg_600x330_0297e8aa.jpg'
              }
          ]
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
        height:0
        padding-bottom: 55%
        background: #ccc
        .swiper-img 
            width: 100%
</style>