<template>
  <div class="tool-box">
    <div class="tool-cn">
      <div class="iconfont">
        &#xe60d;
        <p>电话预定</p>
      </div>
      <div class="iconfont iconfont2">
        &#xe78e;
        <p>下载客户端</p>
        </div>
      <div class="iconfont iconfont3">
        &#xe622;
        <p>我的</p>
      </div>
    </div>
    <div class="c_callcenter">网站地图｜电脑版</div>
    <p>©2018携程旅行｜沪ICP备08023580号</p>
  </div>
</template>

<script>
export default{
  name: 'HomeRecommend',
  props: {
    list: Array
  }
}
</script>

<style scoped>

.tool-box{
  margin-top: 10px;
  text-align: center;
  height: 111px;
}
.tool-cn{
 height: 51px;
 margin-bottom:5px;
 background-color:#fff;
 overflow:hidden;
}
.c_callcenter{
  height: 21px;
  color:#666;
  font:12px;
}
.tool-box p{
  padding:5px 0;
  color:#999;
  font-size:12px;
}
.iconfont{
  font-size: 23px;
  padding-top: 10px;
  height:80% ;
  width: 33%;
  float: left;
}
.iconfont p{
  margin-top: 3px;
  padding: 0 0 0 0;
}
</style>
