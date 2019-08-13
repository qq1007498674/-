
<template>
  <div class="guding" id="one">
    <div class="yuanquan">
            <span style=""><a style class="el-icon-arrow-left"></a></span>
            <span style="margin-top:6%;matgin-left:-3px"><a>丨</a></span>
            <span><a style class="el-icon-s-operation"></a></span>
        </div>
        <a href="#one"><img calss="img" 
          style="position:absolute;width: 11%;bottom:11%;right:3%; z-index: 11;
          position: fixed;" 
          src="./images/2345.png"></a>
    <div class="ull">
      <ul>
        <li>
          <a style="color:#fff" class="el-icon-back"></a>
        </li>
        <li style>
          <a style="color:#fff" class="el-icon-s-operation"></a>
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
          <a style="color:#fff" class="el-icon-s-grid"></a>
        </li>
      </ul>
    </div>
    <div class="zhong">
      <img src="./images/烧鸡.jpg" alt />
      <div class="zhongone">
        <h5 >脆皮辣汁BB鸽</h5>
        <div class="tags">
          <span class="tag">粤菜</span>
          <span class="tag">家禽</span>
          <span class="tag">咸菜</span>
          <span class="tag">热菜</span>
        </div>
        <div class="more">
          <p>
            <span>1815</span>"人气指数"
          </p>
        </div>
        <div class="pgc_yjx">
          <!-- ::before -->
          <p>采用腌制的手法，去除家禽本身的腥味，增加香味。整道菜式风味足，更为咸鲜诱人。</p>
        </div>
      </div>

      <div class="theme">
        <a href class="img">
          <span class="top_title">来自精选专题</span>
          <img class="img1" src="./images/b.jpg" />
          <a class="title" style="text-align: left">五香风味菜 一箸入口齿唇留香</a>
        </a>
      </div>
      <ul>
        <li>
          <a href="#">食材用料</a>
        </li>
        <li>
          <a href="#">食材用料</a>
        </li>
        <li>
          <a href="#">食材用料</a>
        </li>
        <li>
          <a href="#">食材用料</a>
        </li>
      </ul>
    </div>
    <!-- 食材用料 -->
    <div class="recipe-more" style="">
      <h5 >食材用料</h5>
      <div class="zhufu">
        <div class="zhu">
          <h6>
            <i class="el-icon-chicken"></i>
            主料
          </h6>
          <div class="zhuliao">
            <p >
              <span style="margin-left:22px">乳鸽（10天BB鸽）</span>
              <span  class="er" >1只</span>
            </p>
          </div>
        </div>
        <!-- 辅料 -->
          <div class="zhu">
            <h6>
              <i class="el-icon-chicken"></i>
              辅料
            </h6>
            <div class="zhuliao">
              <ul >
                <li>
                  <p>
                    <span >
                      <a style="color:#ff6a00" href="#">家乐辣鲜露</a>
                    </span>
                    <span class="er" >5克</span>
                  </p>
                </li>
                <li>
                  <p>
                    <span style="width:60%">家乐辣鲜露</span>
                    <span class="er" style="width:40%; ">5克</span>
                  </p>
                </li>
                <li>
                  <p>
                    <span style="width:60%">家乐辣鲜露</span>
                    <span class="er" style="width:40%; ">5克</span>
                  </p>
                </li>
              </ul>
            </div>
          
          <hr class="hr" />
          <div class="penren">
            <h5>烹饪步骤</h5>

            <div class="thenr">
              <p>
                <em>1</em>把盐擦匀乳鸽外皮，腌10分钟。用80摄氏度-90摄氏度水烫过；
              </p>
              <p>
                <em>1</em>把盐擦匀乳鸽外皮，腌10分钟。用80摄氏度-90摄氏度水烫过；
              </p>
              <p>
                <em>1</em>把盐擦匀乳鸽外皮，腌10分钟。用80摄氏度-90摄氏度水烫过；
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="tupian">
      <a class="img">
        <img src="./images/c.png" alt />
      </a>
    </div>
    <div class="caishi">
      <p>
        <img src="./images/22.png" />
        <a>相关产品</a>
        <img src="./images/11.png" />
      </p>
      <div class="zhongone1">
       <a class="img"><img src="./images/abc.jpg"></a>
       <div class="jiale">
       <h3
       style="margin: 8px 15px 8px 0px;">家乐辣鲜露</h3>
       <p >独特配方让新鲜的辣味和鲜味达到完美</p>
       </div>
      </div>
      
    </div>
    <div class="chanp">
    <p>
        <img src="./images/22.png" />
        <a>相关菜式</a>
        <img src="./images/11.png" />
      </p>
      </div>
      <div class="ui">
        <el-row :gutter="20">
      <el-col style="margin-top: -17px;" :span="12">
        <div class="grid-content bg-purple">
          <p>
            <img style="width:160px" src="./images/33.jpg" />
          </p>
        </div>
      </el-col>

      <el-col style="margin-top: -17px;" :span="12">
        <div class="grid-content bg-purple">
          <p>
            <img style="width:160px" src="./images/33.jpg" />
          </p>
        </div>
      </el-col>
      <div></div>
    </el-row>
    <el-row :gutter="20">
      <el-col :span="12">
        <div
          class="grid-content bg-purple"
          style="background-color:	#FFFFFF; height:56px;width:145px;
                  margin-left: 16px;margin-top: -45px;border-radius: 6px"
        >
          <ul style="list-style:none; margin-right: 9px;line-height: 18px;">
            <li style="font-size:1px;font-weight:bold;">一般的鸡肠</li>
            <li style="color:red;font-size:3px;">3162人气</li>
            <li>
              <a style="margin-left: 4px;font-size:1px;
               color: #857e76;
                background-color: #faf5ef;
                padding: 2px;
                margin: 0 3px;
              ">海鲜 热菜 粤菜</a>
            </li>
          </ul>
        </div>
      </el-col>
      <el-col style="margin-left: 190px;" :span="12">
       <div
          class="grid-content bg-purple"
          style="background-color:	#FFFFFF; height:56px;width:145px;
                  margin-left:23px;margin-top: -55px;border-radius: 6px">
          <ul style="list-style:none; margin-right: 9px;line-height: 18px;">
            <li style="font-size:1px;font-weight:bold;">一般的鸡肠</li>
            <li style="color:red;font-size:3px;">3162人气</li>
            <li>
              <a style="margin-left: 4px;font-size:1px">海鲜 热菜 粤菜</a>
            </li>
          </ul>
        </div>
      </el-col>
    </el-row>
      </div>
      <div>
        <div class="ui">
          <el-row :gutter="20">
      <el-col style="margin-top: -17px;" :span="12">
        <div class="grid-content bg-purple">
          <p>
            <img style="width:160px" src="./images/33.jpg" />
          </p>
        </div>
      </el-col>

      <el-col style="margin-top: -17px;" :span="12">
        <div class="grid-content bg-purple">
          <p>
            <img style="width:160px" src="./images/33.jpg" />
          </p>
        </div>
      </el-col>
      <div></div>
    </el-row>
    <el-row :gutter="20">
      <el-col :span="12">
        <div
          class="grid-content bg-purple"
          style="background-color:	#FFFFFF; height:56px;width:145px;
                  margin-left: 16px;margin-top: -45px;border-radius: 6px"
        >
          <ul style="list-style:none; margin-right: 9px;line-height: 18px;">
            <li style="font-size:1px;font-weight:bold;">一般的鸡肠</li>
            <li style="color:red;font-size:3px;">3162人气</li>
            <li>
              <a style="margin-left: 4px;font-size:1px;
               color: #857e76;
                background-color: #faf5ef;
                padding: 2px;
                margin: 0 3px;
              ">海鲜 热菜 粤菜</a>
            </li>
          </ul>
        </div>
      </el-col>
      <el-col style="margin-left: 190px;" :span="12">
       <div
          class="grid-content bg-purple"
          style="background-color:	#FFFFFF; height:56px;width:145px;
                  margin-left:23px;margin-top: -55px;border-radius: 6px">
          <ul style="list-style:none; margin-right: 9px;line-height: 18px;">
            <li style="font-size:1px;font-weight:bold;">一般的鸡肠</li>
            <li style="color:red;font-size:3px;">3162人气</li>
            <li>
              <a style="margin-left: 4px;font-size:1px">海鲜 热菜 粤菜</a>
            </li>
          </ul>
        </div>
      </el-col>
    </el-row>
        </div>
       
      </div>

      <div class="chanp">
    <p>
        <img src="./images/22.png" />
        <a>留言评论（6）</a>
        <img src="./images/11.png" />
      </p>
      </div>
      <div class="tupi">
        <a><img src="./images/abcd.jpg"></a>
        <h3>钟明</h3>
        <p>卖相还可以</p>
        <span>举报</span>
        <i class="el-icon-chat-dot-square"><span>0</span></i>
      </div>

      <div class="tupi">
        <a><img src="./images/abcd.jpg"></a>
        <h3>钟明</h3>
        <p>卖相还可以</p>
        <span>举报</span>
        <i class="el-icon-chat-dot-square"><span>0</span></i>
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
<style>
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
    margin-top: 4.5%;
    margin-left: 1%;
    padding: 1px;
}
.yuanquan{
    position: fixed;
    height: 4.7%;
    top:86%;
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

.tupi{
  width: 90%;
  background-color:#fff;
  height: 100px;
  margin-left: 5%;
  margin-top: 20px;
  line-height: 30px;
}
.tupi i{
  margin-left: 50%;
}
.tupi span{
    margin-left:2%; 
  font-size: 13px;
  color: #857e76;
}
.tupi p{
  margin-left:-46%; 
  font-size: 13px;
  margin-top: 2%
}
.tupi h3{
  margin-left:-56%; 
  font-size: 13px;
  margin-top: -12%
}
.tupi img{
  width: 10%;
  /* 把图片搞圆 下两句*/
  border-radius: 50%;
    height: auto;
    margin-left: -80%;
    margin-top: 2%;
}
.ui{
  margin-top: 10%;
}
.chanp{
  margin-top: 6%;
}
.caishi .zhongone1 .jiale{
  margin-top: -28%;
}
.caishi .zhongone1 .jiale p{
  margin-left: 39%;
  font-size: 10px;
  /* margin: 8px 15px 8px 0px; */
}
.caishi .zhongone1 .img img{
  width: 30%;
  margin-left: -65%;
  
}
.caishi .zhongone1 {
  margin-left: 5%;
  margin-top: 5%;
  height: 110px;
  padding: 10px 0;
  width: 90%;
  font-size: 10px;
  display: flex;
  background-color: #fff;

  
    border-radius: 15px;
    display: block;
    text-align: center;
    padding: 5px 0;
}
.caishi .zhongone  p{
  margin-top: -50px;
}
.caishi  {
  margin-top: 8%;
  /* margin-top: 20%;
  height: 240px;
  position: relative;
  background-color: #ffffff;
  border-radius: 5px;
  margin: -50px 10px 10px 10px;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
  padding: 30px 0; */
}
.tupian .img img {
  width: 100%;
  height: auto;
  border-radius: 5px;
}
.penren {
  margin-top: 9%;
}
.thenr p em {
  font-weight: normal;
  font-style: normal;
  color: #ffffff;
  font-size: 12px;
  text-align: center;
  background-color: #ff8000;
  border-radius: 50%;
  flex-shrink: 0;
  line-height: 18px;
  width: 18px;
  height: 18px;
  margin-right: 8px;
}
.thenr p {
  font-size: 14px;
  color: #857e76;
  display: -webkit-flex;
  display: -moz-flex;
  display: flex;
  margin: 15px 0;
}
.zhufu .hr {
  margin-top: 30px;
  margin-left: -5%;
  width: 110%;
}
.zhuliao ul{
  list-style: none;
}
.zhuliao span{
  text-align: right
}
.zhuliao p {
  
  border-bottom: 1px solid #857e76;
  font-size: 12px;
  /* display: -webkit-flex;
  display: -moz-flex;
  display: flex; */
  -webkit-flex-wrap: wrap;
  flex-wrap: wrap;
  padding: 10px 0;
  border-color: #faf5ef;
  width:94%;
}
.zhuliao p span {
  font-size: 9%;
  margin-left: 20%;
}
.zhuliao {
   width: 100%;
 display: flex;
 flex-direction: column
}
/* .zhuliao p .er{
  margin-left: 16%;
} */
.el-icon-chicken {
  color: #ff6a00;
  font-size: 18px;
}
h6 {
  color: #857e76;
}
.zhu {
  
  width: 94%;
  text-align: left
}

/* 食材用料区域 */
.recipe-more {
  width: 97%;
  position: relative;
  background-color: #ffffff;
  border-radius: 5px;
  margin: 0 10px;
  padding: 30px 20px;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
  margin-bottom: 15px;
  display: flex;
  flex-direction: column;
}
.recipe-more h5 {
 margin-left: 0px;
 text-align: left;
  font-weight: bold;
  font-size: 1.13em;
}
/* 食材用料文字 */
.zhong ul {
  display: flex;
  list-style: none;
  margin-left: 13%;
  margin-top: 4%;
  margin-bottom: 5%;
}
.zhong li {
  padding-left: 5%;
  font-size: 12px;
}
a {
  text-decoration: none;
  color: #857e76;
}
.zhong ul li a:hover {
  color: black;
  position: relative;
}
.tab ul li.active {
  color: #ff8000;
  position: relative;
}
/* 4、图片 */
.theme {
  width: 100%;
  position: relative;
  /* flex-direction: column; */
  margin: 0px auto;
}
.theme .img .top_title {
  display: block;
  position: absolute;
  width: 94%;
  margin-top: 0%;
  padding: 10px 20px;
  text-align: left;
  font-size: 14px;
  color: #fff;
  background-color: rgba(0, 0, 0, 0.5);
  border-top-left-radius: 5px;
  border-top-right-radius: 5px;
  margin-left: 13px;
}
.theme .img .title {
  position: absolute;
    bottom: 3px;
    left: 9px;
    width: 97%;
    color: #ffffff;
    font-size: 18px;
    line-height: 1.5em;
    font-weight: 400;
    padding: 18px;
    padding-bottom: 20px;
    padding-top: 20px;
    letter-spacing: 1px;
    background: linear-gradient(to bottom, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8));
    border-bottom-left-radius: 5px;
    border-bottom-right-radius: 5px;
}
.theme .title a{
     margin-left: -30px
 
  
  
 
 
} 
.theme .img1 {
  width: 97%;
  height: auto;
  border-radius: 5px;
}

/* 碎皮辣汁鸡 */
.pgc_yjx {
  position: relative;
  padding: 15px 4px;
  margin: 0 20px;
  margin-top: 30px;
  border: 1px solid #dfdedb;
  border-radius: 10px;
  border-left-color: transparent;
  border-right-color: transparent;
}
.pgc_yjx:before {
  position: absolute;
  color: #857e76;
  background-color: #ffffff;
  font-size: 12px;
  padding: 0 1em;
  letter-spacing: 0.1em;
  top: -0.8em;
  left: calc(50% - 3.3em);
  content: "菜式特色";
}
.pgc_yjx p {
  position: relative;
  color: #857e76;
  font-size: 12px;
  line-height: 1.5em;
  padding: 0 2.5em;
}
.zhongone .more p {
  font-size: 12px;
  color: #857e76;
  letter-spacing: 0.04em;
}
p {
  margin: 0;
  font-weight: normal;
  line-height: 1.3em;
}
h5 {
  margin-left: -60%;
  font-size: 18px;
  font-weight: normal;
  font-style: normal;
  color: #2f2a26;
  margin-bottom: 8px;
}
.zhong{
  width: 100%;
}
.zhongone .more {
  margin-top: 5%;
  margin-left: -60%;
}
.zhongone .more p span {
  font-size: 20px;
  color: #ff8000;
  margin-right: 8px;
}
.zhongone .tags {
  margin-left: -43%;
}
.zhongone .tags .tag {
  font-size: 12px;
  color: #857e76;
  padding: 3px 8px;
  margin-right: 5px;
  background-color: #faf5ef;
}
.zhongone {
  height: 240px;
  position: relative;
  background-color: #ffffff;
  border-radius: 5px;
  margin: -50px 10px 10px 10px;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
  padding: 30px 0;
}
.guding {
  background-color: rgb(250, 245,239);
  height: 3000%;
  margin-top: -59px;
}
.zhong img {
  width: 100%;
}

/* 以下是输入框 */
.guding {
  box-sizing: border-box;
}
.ull {
  width: 100%;
  display: flex;
  flex-direction: column;
  height: 9%;
  position: fixed;
  z-index: 12;
  box-sizing: border-box;
  background: linear-gradient(to right, #ff6a00, #ff9700);
}
.ull ul {
  margin-top: 2%;
  list-style: none;
  display: flex;
  width: 100%;
}
.ull ul li{
  line-height:8%;
}
.ull li:nth-child(1) {
  margin-left: 5%;
  font-size: 180%;
  margin-top: 2%;
  color: #fff;
  width: 30px;
}
.ull li:nth-child(2) {
  margin-left: 5%;
  font-size: 180%;
  margin-top: 2%;
  color: #fff;
   width:30px;
}
.ull li:nth-child(3) {
  width: 88%;
  margin-left: -15%;
  color: #fff;
  flex:1;
}
.ull li:nth-child(4) {
  margin-left: -15%;
  font-size: 180%;
  margin-top: 2%;
  color: #fff;
  width: 60px;
}
.mint-searchbar {
  background: linear-gradient(to right, #ff6a00, #ff9700);
}

.inp {
  margin-left: 20%;
  height: 7%;
  width: 60%;
  z-index: 11;
}
</style>
