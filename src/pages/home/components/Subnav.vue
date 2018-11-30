<template>
    <ul class="subnav-entry">
      <li class="subnav" v-for="item of list" :key="item.id">
        <img class="icon_img_style" :src="item.icon" alt="">
        <p class="subnav_desc">{{item.desc}}</p>
      </li>
    </ul>
</template>
<script>
export default{
  name: 'HomeSubnav',
  props: {
    list: Array
  }
}
</script>
<style scoped>
.subnav-entry{
  width: 98%;
  margin: auto;
  height: 116px;;
  border-radius:8px;
  background-color: rgb(255, 255, 255);
  box-shadow :0 1px 2px rgba(0,0,0,.2);
}
.subnav{
  text-align: center;
  height: 10px;
}
.subnav-entry li{
  height: 50%;
  width: 20%;;
  float: left;
}
.subnav img{
  height: 66%;
}
.subnav p{
  font-size: 10px;
  text-align: center;
}
</style>
