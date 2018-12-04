<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item in list" :key="item.id">
        <a :href="item.Url">
        <img class="swiper_img" :src="item.imgUrl" alt="">
        </a>
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default{
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data: function () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay:3000
      }
    }
  }
}
</script>

<style scoped>
  .swiper_img{
    width: 100%;
  }
  .wrapper >>> .swiper-pagination-bullet-active{
    background: #fff !important
  }
</style>
