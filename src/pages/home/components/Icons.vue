<template>
  <div class="icons">
    <div class="icon" v-for="item of list" :key="item.id" onclick="window.open('http://m.ctrip.com/webapp/myctrip/?from=http%3A%2F%2Fm.ctrip.com%2Fhtml5%2F','_self')">
      <div class="icon_img">
        <img class="icon_img_style" :src="item.imgUrl" alt="">
      </div>
      <p class="icon_desc">{{item.desc}}</p>
    </div>
  </div>
</template>

<script>
export default{
  name: 'HomeIcons',
  props: {
    list: Array
  }
}
</script>

<style scoped>
  /*border-radius:18px;
    background-color: rgb(255, 255, 255)*/
  .icons{
    box-shadow :0 1px 2px rgba(0,0,0,.2);
    margin:auto;
    width: 98%;
    font-size: .8em;
    padding-top:0.12rem;
    height:1.1rem;
    margin-top:.1rem;
    border-radius:8px;
    background-color: rgb(255, 255, 255);
  }
  .icon{
    position: relative;
    overflow: hidden;
    float: left;
    height: 100%;
    width: 20%;
    /* background-color: red; */
  }
  .icon_img{
    height: 100%;
  }
  .icon_img_style{
    display: block;
    height: 50%;
    margin: 0 auto;
  }
  .icon_desc{
    position: absolute;
    bottom: 0.45rem;
    left: 0;
    right: 0;
    height: .14rem;
    line-height: .64rem;
    text-align: center;
    color: #333;
  }
</style>
