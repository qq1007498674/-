<template>
  <div class="shouye">
    <div>
      <mt-search  class="inp"
       v-model="value" cancel-text="取消" placeholder="搜索菜谱和问答..."></mt-search>
    </div>
    <div class="ull">
    <p>菜系</p>
    <ul class="uls" style="margin-top:50px;">
        <li class="lis" style="background-color: #ff8000;"><a href="#">全部</a></li>
        <li class="lis" v-for="(item,index) in list " :key="index"><a href="#">{{item}}</a></li>
    </ul>
    </div>

    <div class="ull">
    <p>菜系</p>
    <ul class="uls" style>
        <li class="lis" style="background-color: #ff8000;"><a href="#">全部</a></li>
        <li class="lis" v-for="(item,index) in list " :key="index"><a href="#">{{item}}</a></li>
    </ul>
    </div>

    <div class="ull">
    <p>菜系</p>
    <ul class="uls" style>
        <li class="lis" style="background-color: #ff8000;"><a href="#">全部</a></li>
        <li class="lis" v-for="(item,index) in list " :key="index"><a href="#">{{item}}</a></li>
    </ul>
    </div>
    <div class="bottom">
        <ul>
            <li style="width:40%;background-color:#FFF4E8;"><a style="color: #ff8000;">取消</a></li>
            <li style="width:60%;background-color: #ff8000;"><a style="color: #FFF4E8;">查看全部</a></li>
        </ul>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      value: "",
      list: [
        "鲁菜",
        "京菜",
        "东北菜",
        "豫菜",
        "鲁菜",
        "京菜",
        "东北菜",
        "豫菜",
        "鲁菜",
        "京菜",
        "东北菜",
        "豫菜",
        "鲁菜",
        "京菜",
        "东北菜",
        "豫菜",
        "鲁菜",
        "京菜",
        "东北菜",
        "豫菜",
        "鲁菜",
        "京菜",
        "东北菜",
      ]
    };
  }
};
</script>
<style lang="css">
.mint-searchbar-cancel {
    color:rgba(255, 255, 255, 0.8);
    font-size: 10%;
    
}
.mint-searchbar{
   background: linear-gradient(to right, #ff6a00, #ff9700);
}
.inp{
   
    height: 7%;
    width: 100%;
    position: fixed;
    left: 0px;
    top: 0px;
    z-index: 11;
}
a{
     text-decoration: none;
    
}
.ull{
    margin-left: 15px;
    margin-top: 20px;
    
}
ul{
    /* 块级元素 */
    display: -webkit-flex;
    display: -moz-flex;
    display: flex;
    -webkit-flex-wrap: wrap;
    list-style: none;
    font-size: 14px;
    
}
.lis{
    width: 22%;
    border: 1px solid #C2BCB5;
    border-radius: 4px;
    text-align: center;
    padding: 5px 0px;
    letter-spacing: .1em;
    margin-bottom: 10px;
    margin-right: 10px;
    /*平均的宽度平分*/
    width: calc( ( 100% - 50px ) / 4 );
    display: list-item;
    
}
.lis a{
    color: #000;
}
* {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    -moz-appearance: none;
    -ms-appearance: none;
    -o-appearance: none;
    appearance: none;
}
.shouye {
  margin-top: -61px;
}
p{
   margin-left: -90%; 
   margin-bottom:15px;
}
.bottom{
    
    line-height: 349%;
    width: 100%;
    position: fixed;
   
    bottom: 0px;
    z-index: 11;
}
</style>
