<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/201406/09/9b6a236005af2a74aad1ed2dadf8e5b6.jpg_600x330_6d254a92.jpg" />
      <div class="banner-info">
        <div class="banner-title">雪窦山</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe72e;</span>
          10
        </div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/201406/09/9b6a236005af2a74aad1ed2dadf8e5b6.jpg_r_800x800_1692ae93.jpg', 'http://img1.qunarzz.com/sight/p0/201406/09/7c02b0eda40baa5c707f6f24e172b978.jpg_r_800x800_14e33e19.jpg', 'http://img1.qunarzz.com/sight/p0/1412/4d/11d15f2de922b2ef09d59d44ab635530.water.jpg_r_800x800_9dcef1a2.jpg']
    }
  },
  components: {
    CommonGallary
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
    .banner-img
      width:100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 1))
      .banner-title
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        line-height: .32rem
        height: .32rem
        margin-top: .14rem
        padding: 0 .32rem
        border-radius: .2rem
        background: rgba(0, 0, 0, .5)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
