<template>
    <div class="Row">
        <div class="sales-hd">

        </div>
        <div class="sales-bd">

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
    height: 44px;
    background: black;
}
.sales-bd{
    background-color: aquamarine;
    padding:8px;
    padding-top: 0px;
}
</style>
