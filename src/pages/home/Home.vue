<template>
<div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-recommend></home-recommend>
    <home-weekend></home-weekend>
</div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
<<<<<<< HEAD
import axios from 'axios'
=======
import HomeWeekend from './components/Weekend'
>>>>>>> home-weekend
export default {
    name: 'Home',
    components: {
        HomeHeader,
        HomeSwiper,
        HomeIcons,
<<<<<<< HEAD
        HomeRecommend
    },
    methods:{
        getHomeInfo(){
            axios.get('/api/index.json')
                .then(this.getHomeInfoSucc)
        },
        getHomeInfoSucc(res){
            console.log(res)
        }

    },
    mounted () {
        this.getHomeInfo()
=======
        HomeRecommend,
        HomeWeekend
>>>>>>> home-weekend
    }
}
</script>

<style scoped>
</style>
