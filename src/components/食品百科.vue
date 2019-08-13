<template>
  <div class="home">
    <div class="test">
        <div class="yuanquan">
            <span style=""><a style class="el-icon-arrow-left"></a></span>
            <span style="margin-top:8%"><a>1234丨123</a></span>
            <span><a style class="el-icon-s-operation"></a></span>
        </div>
        <img calss="img" 
          style="position:absolute;width: 11%;bottom:11%;right:3%; z-index: 11;
          position: fixed;" 
          src="./images/2345.png">
      <div class="guding">
        <div class="ull">
          <ul>
            <li>
              <a style class="el-icon-back"></a>
            </li>
            <li style>
              <a style class="el-icon-s-operation"></a>
            </li>
            <li>
              <mt-search
                style="height: 130%;"
                class="inp"
                v-model="value"
                cancel-text="取消"
                placeholder="搜索菜谱和问答..."
              ></mt-search>
            </li>
            <li>
              <a style class="el-icon-s-grid"></a>
            </li>
          </ul>
        </div>
        <mt-navbar class="page-part" v-model="selected">
          <mt-tab-item id="1">食品百科</mt-tab-item>
          <mt-tab-item id="2">食品微讲堂</mt-tab-item>
          <mt-tab-item id="3">食品头条</mt-tab-item>
        </mt-navbar>
      </div>
      <div class="ull2" >
        <mt-tab-container v-model="selected" >
          <mt-tab-container-item id="1" style="margin-top:-20px">
            <ul v-for="(n,index) in 6" :key="index">
              <li>
                <img src="./images/1234.jpeg" />
              </li>
              <li>
                <h5>食安“国宝级”培训课程免费送啦！</h5>
              </li>
              <li>
                <span>采用碎片化时间，随时随地在线学习，将基础知识应用于实践，提升从业水平。</span>
              </li>
            </ul>
          </mt-tab-container-item>
          <mt-tab-container-item id="2">
            <!-- <mt-cell v-for="(n,index) in 4" :title="'测试 ' + n" :key="index" /> -->
            <ul v-for="(n,index) in 6" :key="index">
              <li>
                <img src="./images/1234.jpeg" />
              </li>
              <li>
                <h5>食安“国宝级”培训课程免费送啦！</h5>
              </li>
              <li>
                <span>采用碎片化时间，随时随地在线学习，将基础知识应用于实践，提升从业水平。</span>
              </li>
            </ul>
          </mt-tab-container-item>
          <mt-tab-container-item id="3">
            <ul v-for="(n,index) in 6" :key="index">
              <li>
                <img src="./images/1234.jpeg" />
              </li>
              <li>
                <h5>食安“国宝级”培训课程免费送啦！</h5>
              </li>
              <li>
                <span>采用碎片化时间，随时随地在线学习，将基础知识应用于实践，提升从业水平。</span>
              </li>
            </ul>
          </mt-tab-container-item>
        </mt-tab-container>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "page-navbar",
  value: "",
  data() {
    return {
      value: "",
      selected: "1"
    };
  }
};
</script>
<style lang="css">

* {
  margin: 0px;
  padding: 0px;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  -webkit-text-size-adjust: none;
  text-size-adjust: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  -ms-appearance: none;
  -o-appearance: none;
  appearance: none;
}
span{
    /* display: flex;
    flex-grow: 1;
    justify-content: center;
    line-height: 1rem;
    position: relative; */
    margin-top: 10%;
    padding: 1px;
}
.yuanquan{
    position: fixed;
    height: 4.7%;
    top:79%;
    bottom: 7.5rem; 
    left: 15px;
    /* background: rgba(250,250,250,.95); */
    background: rgba(250,250,250,.95);
    width: 5.5rem;
    line-height: 1rem;
    border-radius: 0.9rem;
    border: 1px solid #c2bcb5;
    display: flex;
    justify-content: space-around;
    z-index: 11;
    justify-content: center;
    font-size: 18px;
}
.guding{
  
     box-sizing: border-box;
}
.ull{
    width: 100%;
   position: fixed;
   z-index: 12;
     box-sizing: border-box;
     background: linear-gradient(to right, #ff6a00, #ff9700);
}
.page-part {
    width: 100%;
    margin-top: 0%;
    background: linear-gradient(to right, #ff6a00, #ff9700);
   position: fixed;
   z-index: 11;
   top:5%;
}
.ull2{
    position: relative;
    top:160%
}
.ull2 ul {
    margin-top: 10px;
  list-style: none;
  width: 89%;
  height: 220px;
  background-color: #fff;
  margin-left: 5.5%;
  margin-top: 6%;
  border-radius: 5px;
  overflow: hidden;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
  margin-bottom: 15px;
}
.ull2 ul li img {
  width: 100%;
}
.ull2 li:nth-child(2) {
  font-size: 20px;
  margin-left: -12%;
}
.ull2 li:nth-child(3) {
  margin-left: 6%;
  font-size: 12px;
  color: #857e76;
  margin-top: 2%;
}


.ull ul {
  list-style: none;
  display: flex;
}
.ull li:nth-child(1) {
  margin-left: 5%;
  font-size: 180%;
  margin-top: 2%;
  color: #fff;
}
.ull li:nth-child(2) {
  margin-left: 5%;
  font-size: 180%;
  margin-top: 2%;
  color: #fff;
}
.ull li:nth-child(3) {
  width: 88%;
  margin-left: -15%;
  color: #fff;
}
.ull li:nth-child(4) {
  margin-left: -15%;
  font-size: 180%;
  margin-top: 2%;
  color: #fff;
}
.mint-searchbar {
  background: linear-gradient(to right, #ff6a00, #ff9700);
}

.test {
   position:relative;
   
  width: 100%;
  background: linear-gradient(to right, #ff6a00, #ff9700);
  height: 55px;
  margin-top: -16%;
}
.home {
  min-height: 667px;
  background-color: #faf5ef;
}
.inp {
  margin-left: 20%;
  height: 7%;
  width: 60%;
  z-index: 11;
}
</style>
