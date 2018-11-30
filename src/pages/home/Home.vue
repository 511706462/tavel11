<template>
<div>
    <home-header></home-header>
    <home-swiper :list="swiperList"></home-swiper>
    <home-icons :list="iconsList"></home-icons>
    <home-gridnavs :list="gridnavList"></home-gridnavs>
    <home-subnav :list="subnavlist"></home-subnav>
    <home-row :list="rowlist"></home-row>
    <home-recommend :list="recommendList"></home-recommend>
</div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import HomeGridnavs from './components/Gridnav'
import HomeSubnav from './components/Subnav'
import HomeRow from './components/Row'
import axios from 'axios'
export default{
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeGridnavs,
    HomeSubnav,
    HomeRow,
    HomeRecommend
  },
  data: function () {
    return {
      swiperList: [],
      iconsList: [],
      recommendList: [],
      gridnavList: [],
      subnavlist: [],
      rowlist: []
    }
  },
  methods: {
    getHomeInfo: function () {
      axios.get('/api/index.json').then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc: function (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.swiperList = data.swiperList
        this.iconsList = data.iconsList
        this.gridnavList = data.gridnavList
        this.subnavlist = data.subnavlist
        this.recommendList = data.recommendList
        this.rowlist = data.rowlist
      }
      console.log(res)
    }
  },
  mounted: function () {
    this.getHomeInfo()
  }
}
</script>

<style>
body{
  margin: auto;
  max-width: 613px;
  min-width: 310px;
}
</style>
