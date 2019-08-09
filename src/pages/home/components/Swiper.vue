<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
        <!-- slides -->
        <swiper-slide v-for="item of swiperList" :key="item.id">
          <img class="swiper-img" :src="item.imgUrl" />
        </swiper-slide>
        <!-- Optional controls -->
        <!-- 如果需要分页器 -->
        <div class="swiper-pagination"  slot="pagination"></div>
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
        id:'0001',
        imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/a685001bbf5e77a203ff8815e953efbe.jpg_945x288_52b6ec01.jpg',
      }, {
        id:'0002',
        imgUrl:'http://h-des-activity-fecp.qunarzz.com/h_des_activity_fe_h_des_activity_fe/973dc1ae0da73a58410186df08ff25cb.jpg',
      }, {
        id:'0003',
        imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/3f5ff03fa0c024b930f515e63ae2c702.jpg_945x288_7dff4510.jpg',
      }]

    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow hidden
    width: 100%
    height: 0
    padding-bottom: 31.25%
    background: #eee
    .swiper-img  
      width: 100% 
</style>