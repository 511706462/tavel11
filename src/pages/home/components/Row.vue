<template>
    <div class="Row">
        <div class="sales-hd">
            <h2 class="title-tmh"></h2>
        </div>
        <div class="sales-bd">
            <div class="seckill-box" v-for="item in list.slice(0,1)" :key="item">
                <a :href="item.Url">
                <img class="icon_img_style" :src="item.imgUrl" alt="">
                <p class="sales-title">{{item.title}}</p>
                <div class="sales-info">¥{{item.desc}}起</div>
                </a>
            </div>
            <div class="sales-ad-box">
                <div class="row-box row-box-top" v-for="item in list.slice(1,2)" :key="item">
                    <a :href="item.Url">
                    <p class="sales-item-title">{{item.desc}}</p>
                    <p class="sales-item-title2">{{item.desc2}}</p>
                    <img class="icon-sales" :src="item.imgUrl" alt="">
                    </a>
                </div>
                <div class="row-box">
                    <div class="sales-list" v-for="item in list.slice(2,4)" :key="item" :class="'sales-list'+item.id">
                        <a :href="item.Url">
                        <p class="sales-item-title3">{{item.desc}}</p>
                        <p class="sales-item-title4">{{item.desc2}}</p>
                        <img class="icon-sales2" :src="item.imgUrl" alt="">
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default{
  name: 'HomeRow',
  props: {
    list: Array
  }
}
</script>
<style scoped>
.Row{
    background-color: #fff;
    margin-top: .1rem;
    height: 263px;
}
.sales-hd{
    margin: 0 8px;
    height: 44px;
}
.sales-bd{
    height: 211px;
    margin: 0 8px;
    padding-top: 0px;
}

.title-tmh{
    position: relative;
    top: 15px;
    height: 18px;
    background-image: url(http://pic.c-ctrip.com/h5/home/un_home_text.png);
    background-size: 78px;
    background-repeat: no-repeat;
    background-position: top left;
}
.c_selling{
    position: relative;
    top: -5px;
    float: right;
    color: red;
}
.seckill-box{
    float: left;
    width: 49.5%;
    height: 100%;
    background-color: #f9f9f9;
}
.row-box-top{
    background-color: #f9f9f9;
    width:100%;
}
.icon_img_style {
    width: 100%;
    height: 70%;
}
.sales-title{
overflow:hidden;
height:20px;
display:-webkit-box;
text-overflow:ellipsis;
-webkit-line-clamp:2;
-webkit-box-orient:vertical;
padding:8px;
}
.sales-info{
    color:#ff495e;
    font-size:18px;
    line-height:1;
    font-weight:400;
    padding: 8px;
}
.sales-ad-box{
    float:right;
    width: 49.5%;
    height: 100%;
}
.row-box{
    height: 49.5%;
    margin-top: 1%;
    margin-left: 1%;
}
.row-box-top{
    margin-top: 0;
    position:relative;/*3.父容器使用相对定位，子元素使用绝对定位后，这样子元素的位置不再相对于浏览器左上角，而是相对于父容器左上角*/
}
 .icon-sales{
    width:20%;
    position: absolute;/*3.父容器使用相对定位，子元素使用绝对定位后，这样子元素的位置不再相对于浏览器左上角，而是相对于父容器左上角*/
    right: 0;
    bottom: 0;
    }
.sales-item-title{
    position: relative;
    left: 8px;
    top:8px;
    color:#fd3a51;
    font-weight:700;
    font-size:14px;
    letter-spacing:.0rem;
}
.sales-item-title2{
    position: relative;
    left:8px;
    top:16px;
    color:#333;
    font-size:.28rem;
}
.sales-list{
    text-align: center;
    height: 100%;
    background-color: #f9f9f9;
    width: 49.5%;
}
.sales-list img{
    height: 35%;
}
.sales-list0002 {
    float: left;
}
.sales-list0003{
    margin-left: 1%;
    float: right;
}
.sales-item-title3,.sales-item-title4,.icon-sales2{
    margin-top: 8px;
}
</style>
