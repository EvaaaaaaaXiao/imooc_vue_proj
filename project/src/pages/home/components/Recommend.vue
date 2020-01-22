<template>
  <div>
    <div class="title">
      热销推荐
    </div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" />
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
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201406/09/9b6a236005af2a74aad1ed2dadf8e5b6.jpg_200x200_a72deb02.jpg',
        title: '雪窦山',
        desc: '让心灵去远行,去雪窦山进行一场禅修之旅吧'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1809/2c/2c6e61da64812082a3.img.jpg_200x200_709f00bc.jpg',
        title: '雅戈尔动物园',
        desc: '野生风情，动物天堂'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1504/93/93f1260f44dbbe38.water.jpg_200x200_e512d31b.jpg',
        title: '罗蒙环球乐园',
        desc: '这里最近很火哦，好多人都在点评它呢！'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    line-height: .8rem
    text-indent: .2rem
    margin-top: .2rem
    background: #eee
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
        background: #ff9300
        padding: 0 .2rem
        margin-top: .16rem
        border-radius: .06rem
        color: #fff
</style>
