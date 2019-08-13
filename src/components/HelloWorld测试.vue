<template>
  <div id="app">
    <!-- 上拦部分 -->
    <div class="guding">
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
      <div class="page-title" v-if="isT">
        <mt-navbar class="page-part" v-model="selected">
          <mt-tab-item id="1">
            <a>装盘美图</a>
          </mt-tab-item>
          <mt-tab-item id="2">
            <a>食材杂谈</a>
          </mt-tab-item>
          <mt-tab-item id="3">
            <a>汁酱配方</a>
          </mt-tab-item>
          <mt-tab-item id="4">
            <a>烹饪技巧</a>
          </mt-tab-item>
        </mt-navbar>
      </div>
    </div>
    
      <mt-tab-container v-model="selected">
        <mt-tab-container-item id="1">
          <!-- 图片九宫格 -->

          <div class="jiugongge">
            <div class="tupian" v-for="(item,index) in lst" :key="index">
              <img style="width:100%" :src="item" />
            </div>
          </div>
        </mt-tab-container-item>
        <mt-tab-container-item id="2">
          <div class="hei">
            <img src="./images/qwe.jpg" />
            <div class="hei1">
              <h5>莴苣一席绿，美味藏传奇</h5>
              <p>每年到了初夏，也就是到了食用蜗居的黄金时节。它的口感鲜爽清脆，营养丰富，被古往今来的食客誉为“碧玉风尾”。</p>
            </div>
          </div>
        </mt-tab-container-item>
        <mt-tab-container-item id="3">
          <mt-cell v-for="(n,index) in 6" :title="'选项 ' + n" :key="index" />
        </mt-tab-container-item>
      </mt-tab-container>
    </div>

    <!-- <div class="jiugongge">
        <div class="tupian"><img src="./images/haozaijian.jpg"></div>
    </div>-->
  </div>
</template>
<script>
export default {
  name: "page-navbar",
  value: "",
  data() {
    return {
      value: "",
      selected: "1",
      lst: [
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/shixiechengpidunyazhi.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/shixiechengpidunyazhi.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/shixiechengpidunyazhi.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/shixiechengpidunyazhi.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/zhuangpanmeitu/haozaijian.jpg"
      ],
      scroll: '',
        isT:false
    }
  },
    methods: {
      menu() {
        this.scroll = document.documentElement.scrollTop || document.body.scrollTop;
         console.log(this.scroll)
         if(this.scroll>180){
        //   console.log(alert("ninhao"))
        this.isT=true
      }else{
          this.isT=false
      }
      }
    },
    mounted() {
      window.addEventListener('scroll', this.menu)
     
    },
};
</script>
<style>
* {
  margin: 0;
  padding: 0;
}
#app {
  margin-top: -8px;
  height: 100%;
  background-color: rgba(250, 245, 239);
}
/* .guding{
  position: fixed;
   z-index: 11;
} */
/*hei  */
.hei {
  width: 94%;
  background-color: #fff;
  margin: 0px auto;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  padding-bottom: 9px;
  border-top-left-radius: 6px;
  border-top-right-radius: 6px;
  border-radius: 5px;
  margin-top: 120px;
}
.hei1 h5 {
  line-height: 2em;
  font-size: 16px;
  width: 100%;
  text-align: left;
  margin-left: 30px;
  margin-top: 20px;
}
.hei1 p {
  text-align: left;
  margin-left: 32px;
  font-size: 16px;
  color: #857e76;
  margin-top: 10px;
  line-height: 1.5em;
  display: -webkit-box;
  max-height: 3em;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 2;
  overflow: hidden;
}
.hei img {
  width: 100%;
  border-top-left-radius: 5px;
  border-top-right-radius: 5px;
}
/* 九宫格 */
.jiugongge {
  width: 100%;
  background-color: rgba(250, 245, 239);
  display: flex;
  flex-wrap: wrap;
  margin: 0 auto;
  margin-top: 120px
}
.jiugongge .tupian {
  width: 28%;
  height: 28%;
  margin: 0 auto;
  margin-top: 0px;
  padding: 5px;
}
.jiugongge .tupian img {
}
/*  */
.mint-navbar .mint-tab-item.is-selected {
  border-bottom: 3px solid #fff;
  color: #fff;
  margin-bottom: -3px;
}
.page-part {
  color: rgba(255, 255, 255, 0.6);
}
.zhongjian {
  box-sizing: border-box;
  margin-top: 1px;
}
.mint-navbar {
  background: linear-gradient(to right, #ff6a00, #ff9700);
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  text-align: center;
}
.page-title {
  margin-bottom: 20px;
  
}
.ull{
  position: fixed;
   z-index: 11;
   width: 100%;
   box-sizing: border-box;
}
.ull ul {
  margin-top: 2%;
  list-style: none;
  display: flex;
  flex-direction: row;
  width: 100%;
  height: 55px;
  background: linear-gradient(to right, #ff6a00, #ff9700);
}

.ull li {
  font-size: 180%;
  line-height: 50px;
}
.ull li:nth-child(1) {
  width: 50px;
}
.ull li:nth-child(2) {
  width: 50px;
}
.ull li:nth-child(3) {
  flex: 1;
  line-height: 0px;
}
.ull li:nth-child(4) {
  width: 50px;
}
.mint-searchbar {
  background: linear-gradient(to right, #ff6a00, #ff9700);

  box-sizing: border-box;

  display: flex;

  margin-top: 0px;
}
/* 取消颜色 */
.mint-searchbar-cancel {
  color: #26a2ff;
  margin-left: 10px;
  text-decoration: none;
  font-size: 16px;
}
</style>
