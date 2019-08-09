<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key='item.id'>
        <img class="item-img" :src='item.imgUrl' />
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
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1709/41/411f234d79457081a3.img.jpg_256x160_3b3b3190.jpg',
        title: '长隆野生动物世界',
        desc: '熊猫三胞胎，与您共享欢乐时光。熊猫三胞胎，与您共享欢乐时光。'
      },{
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1905/e6/e683c8cf5e97ce03a3.img.jpg_256x160_4ed67486.jpg',
        title: '世界之窗',
        desc: '全球微缩景点，精彩演绎、娱乐项目应有尽有。全球微缩景点，精彩演绎、娱乐项目应有尽有'
      },{
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1907/8d/8da769b8a045ec98a3.img.jpg_200x200_f74bf17b.jpg',
        title: '深圳欢乐谷',
        desc: '释放真心的欢乐！全新飓风湾：科技升级引爆狂欢时刻'
      }]
    }
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
  .item
    overflow hidden
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
        border-radius: .86rem
        color: #fff
      

</style>