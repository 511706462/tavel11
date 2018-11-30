<template>
  <div class="gridnavs">

      <div class="allclass" v-for="item of list" :key="item.id" :class="'hotel'+item.id">

        <div class="gridnav11">
          <div class="gridnav_desc">
          <p class="gridnav_desc_style">{{item.desc}}</p>
          </div>
          <div class="gridnav_img">
           <img class="gridnav_img_style" :src="item.imgUrl" alt="">
          </div>
        </div>

        <div class="gridnav12">
          <p class="gridnav_desc2">{{item.desc2}}</p>
          <p class="gridnav_desc3">{{item.desc3}}</p>
        </div>

        <div class="gridnav13">
          <p class="gridnav_desc4">{{item.desc4}}</p>
          <p class="gridnav_desc5">{{item.desc5}}</p>
        </div>
      </div>
  </div>
</template>
<script>
export default{
  name: 'HomeGridnav',
  props: {
    list: Array
  }
}
</script>
<style scoped>
  .gridnavs img{
    height: 45px;;
  }
  .gridnavs{
    max-width: 613px;
    min-width: 310px;
    box-shadow :0 1px 2px rgba(0,0,0,.2);
    overflow:hidden;
    margin : .1rem auto;
    width: 98%;
    height:273px;
    border-radius:8px;
    background-color: rgb(255, 255, 255);
  }
  .allclass{
    border-bottom: 2px solid #fff;
    height: 33.33%;
    overflow:hidden;
  }
  .hotel0001{
    overflow:hidden;
    background:linear-gradient(to right,#fa5956,#fa9b4d);
  }
  .hotel0002{
    background:linear-gradient(to right,#4b8fed,#53bced);
  }
  .hotel0003{
    background:linear-gradient(to right,#34c2aa,#6cd557);
  }
  .hotel0003 img{
    position: absolute;
    height: 90px;
    margin-top: -50px;
    margin-left: -70px;
  }
  .allclass p{
    line-height:46px;
    color: #fff;
  }
  .gridnav_desc{
    height: 50%;
  }
  .gridnav_img{
    height: 50%;
  }
  .gridnav11{
  text-align:center;
  height: 100%;
  width: 33%;
  float: left;
  border-right: 1px solid #fff;
  }
  .gridnav12{
  text-align:center;
  height: 100%;
  width: 33%;
  float: left;
  border-right: 1px solid #fff;
  }
  .gridnav13{
  text-align:center;
  height: 100%;
  width: 33.3%;
  float: right;
  }
  .gridnav_desc2{
    height: 50%;
    border-bottom: 1px solid #fff;
  }
  .gridnav_desc3{
    height: 50%;
  }
  .gridnav_desc4{
    height: 50%;
    border-bottom: 1px solid #fff;
  }
  .gridnav_desc5{
    height: 50%;
  }
</style>
