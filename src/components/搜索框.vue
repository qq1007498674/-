<template>
<div style="min-height: 667px;background-color: #faf5ef;">
  <div class="shouye" >
      <div class="qianru">
          <mt-search style="height: 130%;"  class="inp"
       v-model="value" cancel-text="取消" placeholder="搜索菜谱和问答..."></mt-search>
       <div class="page-navbar">
    <mt-navbar class="page-part" v-model="selected">
      <mt-tab-item id="1">菜谱</mt-tab-item>
      <mt-tab-item id="2">问答</mt-tab-item>
    </mt-navbar>

    <!-- <div>
      <mt-cell class="page-part" title="当前选中">{{ selected }}</mt-cell>
    </div> -->
    <h6>大家都在搜索</h6>
    <mt-tab-container v-model="selected">
      <mt-tab-container-item id="1">
        <!-- <mt-cell v-for="(n,index) in 6" :title="'内容 ' + n" :key="index"/> -->
        <ul style="margin-left:5%;
                    display: flex;list-style: none;
                    display: -webkit-flex;
                    display: -moz-flex;
                    display: flex;
                    -webkit-justify-content: flex-start;
                    justify-content: flex-start;
                    -webkit-flex-wrap: wrap;
                    flex-wrap: wrap;
        ">
            <li>鲜蚝焗杭茄</li>
             <li>金沙蛋黄酱焗烤海鲜山药泥</li>
            <li>金沙鳕鱼柳</li>
            <li>鲜蚝焗杭茄</li>
             <li>金沙蛋黄酱焗烤海鲜山药泥</li>
            <li>金沙鳕鱼柳</li>
        </ul>
       
      </mt-tab-container-item>
      <mt-tab-container-item id="2">
        <mt-cell v-for="(n,index) in 4" :title="'测试 ' + n" :key="index"/>
      </mt-tab-container-item>
      
    </mt-tab-container>
    <p >查看全部分类</p>
  </div>

    </div>
    </div>
    </div>
     
</template>
<script>
export default {
    name: 'page-navbar',
  data() {
    return {
      value: "",
       selected: '1'
      
    };
  }
};
</script>
<style lang="css">
p{
            margin-top: 5%;
            margin-left:33%;
            font-size: 12px;
            color: #ff8000;
            border: 1px solid #857e76;
            border-color: #ff8000;
            padding: 6px 10px;
            border-radius: 3px;
            width:30%
            
}
.mint-navbar .mint-tab-item.is-selected {
  
    font-size: 12px;
    border: 2px solid #857e76;
    border-color: rgba(0, 0, 0, 0);
    display: inline-block;
    color: rgba(255, 255, 255, 0.6);
}
h6{
    margin-left: -280px;
    margin-top: 20px ;
    margin-bottom:17px;
    padding: 0px;
    font-size: 14px;
}
li{
    margin-left: 10%;
    color: #857e76;
    font-size: 14px;
    border: 1px solid #857e76;
    border-radius: 5px;
    border-color: #c2bcb5;
    padding: 4px 10px;
    margin: 0 8px 8px 0;
}
.page-navbar{
    margin-top: -80px;
    
}
.mint-searchbar-cancel {
    color:rgba(255, 255, 255, 0.8);
    font-size: 10%;
    
}
.mint-searchbar{
   background: linear-gradient(to right, #ff6a00, #ff9700);
}
.inp{
   margin-top: -60px;
    height: 7%;
    width: 100%;
  
    z-index: 11;
}
.shouye {
    margin-top: -20px;
    height: 60px;
    background: linear-gradient(to right, #ff6a00, #ff9700);
}
.page-part{
    margin-top: 19%;
    height: 170%;
    background: linear-gradient(to right, #ff6a00, #ff9700);
}
.mint-cell {
   
        
    
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
</style>
