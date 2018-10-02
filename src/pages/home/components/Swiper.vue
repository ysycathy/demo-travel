<template>
    <div class="container">
      <swiper :options="swiperOption" v-if="showswiper">
        <swiper-slide v-for="item of list" :key="item.id">
          <img class="swiper-img" :src="item.imgUrl" />
        </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
    </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: {
          el: '.swiper-pagination'
        },
        loop: true,
        autoplay: true
      }
    }
  },
  computed: {
    showswiper () {
      return this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
  .container >>> .swiper-pagination-bullet-active
    background: #fff
  .container
    overflow: hidden
    height: 0
    width: 100%
    padding-bottom: 31.25%
    background: #eee
    .swiper-img
      width: 100%
</style>
