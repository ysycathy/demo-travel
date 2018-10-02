<template>
  <div>
    <div class="title">周末游推荐</div>
    <ul>
      <li class="border-bottom" v-for="item of list" :key="item.id">
        <div class="wrapper">
          <img class="wrapper-img" :src="item.imgUrl" />
        </div>
        <div class="content">
          <p class="content-title">{{item.title}}</p>
          <p class="content-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .wrapper
    overflow: hidden
    height: 0
    padding-bottom: 31.24%
    .wrapper-img
      width: 100%
  .content
    padding: .1rem
    text-align: center
    .content-title
      line-hieght: .54rem
      font-size: .32rem
      ellipsis()
    .content-desc
      line-height: .4rem
      color: #b6b6b6
      ellipsis()
</style>
