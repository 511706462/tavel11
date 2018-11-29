<template>
<div class="header">
    <div class="header_input">
      <span class="iconfont">&#xe624;</span>
      搜索:目的地/酒店/景点/航班号
    </div>
    <div class="header_right">
      <i class="iconfont">&#xe60b;</i>
      <p>我的</p>
    </div>

</div>
</template>

<script>
export default{
  name: 'HomeHeader'
}
</script>

<style scoped>
  .header{
    display: flex;
    background-color: #f6f6f6;
    color: #2eaae0;
  }
  .header_input{
    box-shadow:0 2px 4px rgba(0,0,0,.2);
    border:1px solid #999;
    flex: 1;
    padding-left: .2rem;
    background: #fff;
    border-radius: .1rem;
    height: .47rem;
    line-height: .47rem;
    margin-top: .12rem;
    margin-left: .2rem;
    color: #666;
  }
  .back_icon{
    text-align: center;
    }

  .header_right{
    height: 45px;
    width: 1.24rem;
    float: right;
    text-align: center;
    }
  .header_right i {
    display:block;
    margin-top: 5%;
    font-size: 20px;
  }
  .header_right p {
    margin-top: 5%;
    font-size: 100%;
    color: #2eaae0;
  }
</style>
