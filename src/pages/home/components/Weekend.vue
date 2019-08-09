<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key='item.id'>
        <div class="item-img-wrapper">
          <img class="item-img" :src='item.imgUrl' />
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
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
        imgUrl: 'https://img1.qunarzz.com/travel/d1/1704/12/64f406d951f993b5.jpg_480x360x95_7f1e77f9.jpg',
        title: '香港迪士尼',
        desc: '香港迪士尼乐园由一个乐园和三间酒店（香港迪士尼乐园酒店、迪士尼好莱坞酒店以及迪士尼探索家度假酒店）组成，致力为宾客提供奇妙迪士尼体验，让所有家庭及不同年龄的宾客乐在其中。乐园度假区于2005年9月开幕，至今已接待数千万来自世界各地的宾客，成为香港受欢迎的旅游热点之一。'
      },{
        id: '0002',
        imgUrl: 'https://img1.qunarzz.com/travel/d1/1703/46/ff11508de0082b5.jpg_480x360x95_80e861ef.jpg',
        title: '东部华侨城',
        desc: '东部华侨城旅游度假区位于中国最美八大海岸之一、风光旖旎的深圳大鹏湾畔，前拥大梅沙黄金海岸，背倚青翠挺拔的梧桐山脉，是集观光旅游、休闲娱乐、户外运动、健康养生、文化品鉴、科普教育等功能于一体的大型综合性国家生态旅游示范区。'
      },{
        id: '0003',
        imgUrl: 'https://img1.qunarzz.com/travel/d5/1805/a1/c454be5ed0fac0b5.jpg_480x360x95_fce10c6c.jpg',
        title: '大梅沙海滨公园',
        desc: '大梅沙海滨公园位于中国深圳市盐田区，是深圳的一个沙滩，于1999年开发，是深圳比较早期开发的海滨公园之一，也是深圳著名的沙滩之一。'
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
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 75%
    .item-img
      width: 100%
  .item-info
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()
      

</style>