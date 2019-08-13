<template>
  <div id="app">
    <el-row  style="  position: fixed;top: 0;left: 0;z-index: 11;">
      <!--1、上栏 -->
      <el-col :span="24">
        <div class="grid-content bg-purple-dark">
          <el-row style="background: linear-gradient(to right, #ff6a00, #ff9700);height: 78px;" class="el-row1" :gutter="15">
            <el-col :span="8">
              <div class="grid-content bg-purple">
                <img style="width:75%;margin-top:14px;margin-left:10px" src="./images/logo-new.png" />
              </div>
            </el-col>
            <el-col :span="10">
              <div class="grid-content bg-purple">
                <el-input style="margin-top:7px;
                background: linear-gradient(to right, #ffa358, #f7b966);
                border: 0 solid #857e76;
                " placeholder="请输入内容" v-model="input" clearable></el-input>
              </div>
            </el-col>
        <!-- 图标 -->
            <el-col :span="6">
              <div class="grid-content bg-purple">
                <a style="margin-top:10px;color:#fff;width:100%" class="el-icon-s-grid"></a>
              </div>
            </el-col>
          </el-row>
        </div>
      </el-col>
    </el-row>
<!-- 2、菜式-->
    <el-row :gutter="20" style="margin-top: 85px; 
      display: -webkit-flex;
    display: -moz-flex;
    display: flex;
    -webkit-justify-content: space-between;
    justify-content: space-between;
    background: linear-gradient(to right, #ff6a00, #ff9700);
    padding: 0 15px 15px 15px;
    padding-bottom: calc(30px);
    ">
      <el-col :span="6">
        <div class="grid-content bg-purple">
          <a class="abiao" href="#">川菜</a>
        </div>
      </el-col>
      <el-col :span="6">
        <div class="grid-content bg-purple">
          <a class="abiao" href="#">粤菜</a>
        </div>
      </el-col>
      <el-col :span="6">
        <div class="grid-content bg-purple">
          <a class="abiao" href="#">海鲜</a>
        </div>
      </el-col>
      <el-col :span="6">
        <div class="grid-content bg-purple">
          <a class="abiao" href="#">凉菜</a>
        </div>
      </el-col>
    </el-row>
<!-- 3、轮播图  -->
    <el-row style="margin-top:-29px">
      <el-col :span="24">
        <div style class="grid-content bg-purple-dark">
          <!-- "margin-top: 20px -->
          <el-carousel :interval="4000" type="card" height="100px">
            <el-carousel-item v-for="(item,index) in lst" :key="index">
              <img style="width:100%" :src="item" />
            </el-carousel-item>
          </el-carousel>
        </div>
      </el-col>
    </el-row>
<!-- 4、热卖菜和菜谱库 -->
    <el-row style=" margin-top: -85px;" :gutter="20">
      <el-col :span="12">
        <div class="grid-content bg-purple">
          <a href="#">
            <img style="width:90%;height:60px" src="./images/6.png" />
          </a>
        </div>
      </el-col>
      <el-col :span="12">
        <div class="grid-content bg-purple">
          <a href="#">
            <img style="width:90%;height:60px" src="./images/7.png" />
          </a>
        </div>
      </el-col>
    </el-row>
    <!-- 5一般的鸡场 -->
    <el-row :gutter="20">
      <el-col :span="6">
        <div class="grid-content bg-purple"></div>
      </el-col>
      <el-col :span="12">
        <div class="grid-content bg-purple">
          <img src="./images/22.png" />
          <a>为你推荐</a>
          <img src="./images/11.png" />
        </div>
      </el-col>
      <el-col :span="6">
        <div class="grid-content bg-purple">
          <a class="el-icon-refresh-right" style="font-size:10px;">换一批</a>
        </div>
      </el-col>
    </el-row>

    <!-- 以下卡片效果 -->
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
                  margin-left: 26px;margin-top: -45px;border-radius: 6px"
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
                  margin-left:51px;margin-top: -55px;border-radius: 6px">
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
                  margin-left: 26px;margin-top: -45px;border-radius: 6px"
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
                  margin-left:51px;margin-top: -55px;border-radius: 6px"
        >
          <ul style="list-style:none; margin-right: 9px;line-height: 18px;">
            <li style="font-size:1px;font-weight:bold;">一般的鸡肠</li>
            <li style="color:red;font-size:3px;">3162人气</li>
            <li>
              <a style="margin-left: 4px;font-size:1px">海鲜 热菜 粤菜</a>
            </li>
          </ul>
        </div>
      </el-col>

      <!-- 6、食品安全 -->
    </el-row>
    <el-row :gutter="20">
      <el-col :span="6">
        <div class="grid-content bg-purple"></div>
      </el-col>
      <el-col :span="12">
        <div class="grid-content bg-purple">
          <img src="./images/22.png" />
          <a>食品安全</a>
          <img src="./images/11.png" />
        </div>
      </el-col>
      <el-col :span="6">
        <div class="grid-content bg-purple">
          <a style="font-size:10px;">查看更多</a>
        </div>
      </el-col>
    </el-row>
    <p style="font-size: 10px;margin-top:-13px;">实用百科 / 行家诀窍 / 食安头条</p>

    <el-row :gutter="20" style="margin-top:-19px;">
      <el-col :span="24">
        <div class="grid-content bg-purple">
          <!-- Swiper -->
          <div class="swiper-container">
            <div class="swiper-wrapper">
              <div class="swiper-slide" style="margin-left: -58px;">
                <img style="width:324px;height: 139px;margin-top: -1px;" src="./images/111.jpg" />
                <p
                  style="font-size:18px;margin-left: -38px;margin-top: -48px;color:#fff"
                >2分钟原料验收科普小剧场</p>
                <p style="margin-left: -38px;margin-top: 30px;">管好这6大环节，食材验收不出错</p>
              </div>
              <div class="swiper-slide">
                <img style="width:324px;height: 139px;margin-top: -1px;" src="./images/111.jpg" />
                <p
                  style="font-size:18px;margin-left: -38px;margin-top: -48px;color:#fff"
                >2分钟原料验收科普小剧场</p>
                <p style="margin-left: -38px;margin-top: 30px;">管好这6大环节，食材验收不出错</p>
              </div>
              <div class="swiper-slide">
                <img style="width:324px;height: 139px;margin-top: -1px;" src="./images/111.jpg" />
                <p
                  style="font-size:18px;margin-left: -38px;margin-top: -48px;color:#fff"
                >2分钟原料验收科普小剧场</p>
                <p style="margin-left: -38px;margin-top: 30px;">管好这6大环节，食材验收不出错</p>
              </div>
              <div class="swiper-slide">
                <img style="width:324px;height: 139px;margin-top: -1px;" src="./images/111.jpg" />
                <p
                  style="font-size:18px;margin-left: -38px;margin-top: -48px;color:#fff"
                >2分钟原料验收科普小剧场</p>
                <p style="margin-left: -38px;margin-top: 30px;">管好这6大环节，食材验收不出错</p>
              </div>
              <div class="swiper-slide">
                <img style="width:324px;height: 139px;margin-top: -1px;" src="./images/111.jpg" />
                <p
                  style="font-size:18px;margin-left: -38px;margin-top: -48px;color:#fff"
                >2分钟原料验收科普小剧场11</p>
                <p style="margin-left: -38px;margin-top: 30px;">管好这6大环节，食材验收不出错</p>
              </div>
              <div class="swiper-slide">
                <img style="width:324px;height: 139px;margin-top: -1px;" src="./images/111.jpg" />
                <p
                  style="font-size:18px;margin-left: -38px;margin-top: -48px;color:#fff"
                >2分钟原料验收科普小剧场</p>
                <p style="margin-left: -38px;margin-top: 30px;">管好这6大环节，食材验收不出错</p>
              </div>
              <div class="swiper-slide">
                <img style="width:324px;height: 139px;margin-top: -1px;" src="./images/111.jpg" />
                <p
                  style="font-size:18px;margin-left: -38px;margin-top: -48px;color:#fff"
                >2分钟原料验收科普小剧场</p>
                <p style="margin-left: -38px;margin-top: 30px;">管好这6大环节，食材验收不出错</p>
              </div>
              <div class="swiper-slide">
                <img style="width:324px;height: 139px;margin-top: -1px;" src="./images/111.jpg" />
                <p
                  style="font-size:18px;margin-left: -38px;margin-top: -48px;color:#fff"
                >2分钟原料验收科普小剧场</p>
                <p style="margin-left: -38px;margin-top: 30px;">管好这6大环节，食材验收不出错</p>
              </div>
            </div>
            <!-- Add Pagination -->
            <div class="swiper-pagination"></div>
          </div>
        </div>
      </el-col>
    </el-row>

    <!--7、 精选专题 -->

    <el-row :gutter="20">
      <el-col :span="6">
        <div class="grid-content bg-purple"></div>
      </el-col>
      <el-col :span="12">
        <div class="grid-content bg-purple">
          <img src="./images/22.png" />
          <a>精选专题2</a>
          <img src="./images/11.png" />
        </div>
      </el-col>
      <el-col :span="6">
        <div class="grid-content bg-purple">
          <a style="font-size:10px;">查看更多</a>
        </div>
      </el-col>
    </el-row>
    <p style="font-size: 10px;margin-top:-13px;">实用百科 / 行家诀窍 / 食安头条</p>
    <el-row :gutter="20" style="margin-top:-19px;">
      <el-col :span="24">
        <div class="grid-content bg-purple">
          <!-- Swiper -->
          <div class="swiper-container">
            <div class="swiper-wrapper">
              <div class="swiper-slide" style="margin-left: -58px;">
                <img style="width:324px;height: 139px;margin-top: -1px;" src="./images/111.jpg" />
                <p
                  style="font-size:18px;margin-left: -38px;margin-top: -48px;color:#fff"
                >2分钟原料验收科普小剧场</p>
                <p style="margin-left: -38px;margin-top: 30px;">管好这6大环节，食材验收不出错</p>
              </div>
              <div class="swiper-slide">
                <img style="width:324px;height: 139px;margin-top: -1px;" src="./images/111.jpg" />
                <p
                  style="font-size:18px;margin-left: -38px;margin-top: -48px;color:#fff"
                >2分钟原料验收科普小剧场</p>
                <p style="margin-left: -38px;margin-top: 30px;">管好这6大环节，食材验收不出错</p>
              </div>
              <div class="swiper-slide">
                <img style="width:324px;height: 139px;margin-top: -1px;" src="./images/111.jpg" />
                <p
                  style="font-size:18px;margin-left: -38px;margin-top: -48px;color:#fff"
                >2分钟原料验收科普小剧场</p>
                <p style="margin-left: -38px;margin-top: 30px;">管好这6大环节，食材验收不出错</p>
              </div>
              <div class="swiper-slide">
                <img style="width:324px;height: 139px;margin-top: -1px;" src="./images/111.jpg" />
                <p
                  style="font-size:18px;margin-left: -38px;margin-top: -48px;color:#fff"
                >2分钟原料验收科普小剧场</p>
                <p style="margin-left: -38px;margin-top: 30px;">管好这6大环节，食材验收不出错</p>
              </div>
              <div class="swiper-slide">
                <img style="width:324px;height: 139px;margin-top: -1px;" src="./images/111.jpg" />
                <p
                  style="font-size:18px;margin-left: -38px;margin-top: -48px;color:#fff"
                >2分钟原料验收科普小剧场</p>
                <p style="margin-left: -38px;margin-top: 30px;">管好这6大环节，食材验收不出错</p>
              </div>
              <div class="swiper-slide">
                <img style="width:324px;height: 139px;margin-top: -1px;" src="./images/111.jpg" />
                <p
                  style="font-size:18px;margin-left: -38px;margin-top: -48px;color:#fff"
                >2分钟原料验收科普小剧场</p>
                <p style="margin-left: -38px;margin-top: 30px;">管好这6大环节，食材验收不出错</p>
              </div>
              <div class="swiper-slide">
                <img style="width:324px;height: 139px;margin-top: -1px;" src="./images/111.jpg" />
                <p
                  style="font-size:18px;margin-left: -38px;margin-top: -48px;color:#fff"
                >2分钟原料验收科普小剧场</p>
                <p style="margin-left: -38px;margin-top: 30px;">管好这6大环节，食材验收不出错</p>
              </div>
              <div class="swiper-slide">
                <img style="width:324px;height: 139px;margin-top: -1px;" src="./images/111.jpg" />
                <p
                  style="font-size:18px;margin-left: -38px;margin-top: -48px;color:#fff"
                >2分钟原料验收科普小剧场</p>
                <p style="margin-left: -38px;margin-top: 30px;">管好这6大环节，食材验收不出错</p>
              </div>
            </div>
            <!-- Add Pagination -->
            <div class="swiper-pagination"></div>
          </div>
        </div>
      </el-col>
    </el-row>
    <!-- 8、精选专题加图片 -->

    
    <el-row :gutter="20" >
      <el-col :span="6" >
        <div class="grid-content bg-purple"></div>
      </el-col>
      <el-col :span="12">
        <div class="grid-content bg-purple">
          <img src="./images/22.png" />
          <a>精选专题22</a>
          <img src="./images/11.png" />
        </div>
      </el-col>
      <el-col :span="6">
        <div class="grid-content bg-purple">
          <a style="font-size:10px;">查看更多</a>
        </div>
      </el-col>
    </el-row>
    <p style="font-size: 8px;margin-top:-43px;">实用百科 / 行家诀窍 / 食安头条</p>
    <el-row :gutter="20" style="margin-top:-19px;">
      <el-col :span="24">
        <div class="grid-content bg-purple">
          <!-- Swiper -->
          <div class="swiper-container">
            <div class="swiper-wrapper">
              <div class="swiper-slide" style="margin-left: -58px;">
                <img style="width:324px;height: 139px;margin-top: -1px;" src="./images/111.jpg" />
                <p
                  style="font-size:18px;margin-left: -38px;margin-top: -48px;color:#fff"
                >2分钟原料验收科普小剧场</p>
                <p style="font-size: 12px;
                          color: #857e76;
                          line-height: 1.5em;
                          display: -webkit-box;
                          height: 3em;
                          margin-top:20px;
                          -webkit-box-orient: vertical;
                          -webkit-line-clamp: 2;
                          overflow: hidden;">云南特色老菜新做，为原本单一的芥末味增添丰富的味型。加入傣味香料，酸辣适中，极具云南特色风味。三文鱼需要提前用柠檬水浸泡去除腥味。</p>
                            <p style="position:relative;
                                      top:0px;
                                      left:-112px;">
                  <img style="display: inline-block;
                        width: 25px;
                        height: 25px;
                        border-radius: 50%;
                        vertical-align: middle;"
                    src="./images/123.jpg"/>
                  <span  class="nickname"
                    style="margin-left: 5px;
                  font-size: 12px;
                  color: #000000;
                  vertical-align: middle;"
                  >鲁艳洪222</span>
                  <span class="address"  style="position: absolute;
                                  font-size: 12px;
                                  top:5px;
                                  right: -110px;
                                  color: #857e76;
                                  vertical-align: middle;
                                  max-width: 12em;
                                  overflow: hidden;
                                  white-space: nowrap;
                                  text-overflow: ellipsis;">上海 闲时蜗居云南菜</span></p>

              </div>
              <div class="swiper-slide">
                <img style="width:324px;height: 139px;margin-top: -1px;" src="./images/111.jpg" />
                <p
                  style="font-size:18px;margin-left: -38px;margin-top: -48px;color:#fff"
                >2分钟原料验收科普小剧场</p>
                <p style="font-size: 12px;
                          color: #857e76;
                          line-height: 1.5em;
                          display: -webkit-box;
                          height: 3em;
                          -webkit-box-orient: vertical;
                          -webkit-line-clamp: 2;
                          overflow: hidden;">云南特色老菜新做，为原本单一的芥末味增添丰富的味型。加入傣味香料，酸辣适中，极具云南特色风味。三文鱼需要提前用柠檬水浸泡去除腥味。</p>
                            <p style="position:relative;
                                      top:-20px;
                                      left:-117px;">
                  <img style="display: inline-block;
                        width: 25px;
                        height: 25px;
                        border-radius: 50%;
                        vertical-align: middle;"
                    src="./images/123.jpg"/>
                  <span  class="nickname"
                    style="margin-left: 5px;
                  font-size: 12px;
                  color: #000000;
                  vertical-align: middle;"
                  >鲁艳洪222</span>
                  <span class="address"  style="position: absolute;
                                  font-size: 12px;
                                  top:5px;
                                  right: -110px;
                                  color: #857e76;
                                  vertical-align: middle;
                                  max-width: 12em;
                                  overflow: hidden;
                                  white-space: nowrap;
                                  text-overflow: ellipsis;">上海 闲时蜗居云南菜</span></p>
              </div>
              <div class="swiper-slide">
                <img style="width:324px;height: 139px;margin-top: -1px;" src="./images/111.jpg" />
                <p
                  style="font-size:18px;margin-left: -38px;margin-top: -48px;color:#fff"
                >2分钟原料验收科普小剧场</p>
                <p style="font-size: 12px;
                          color: #857e76;
                          line-height: 1.5em;
                          display: -webkit-box;
                          height: 3em;
                          -webkit-box-orient: vertical;
                          -webkit-line-clamp: 2;
                          overflow: hidden;">云南特色老菜新做，为原本单一的芥末味增添丰富的味型。加入傣味香料，酸辣适中，极具云南特色风味。三文鱼需要提前用柠檬水浸泡去除腥味。</p>
                            <p style="position:relative;
                                      top:-20px;
                                      left:-117px;">
                  <img style="display: inline-block;
                        width: 25px;
                        height: 25px;
                        border-radius: 50%;
                        vertical-align: middle;"
                    src="./images/123.jpg"/>
                  <span  class="nickname"
                    style="margin-left: 5px;
                  font-size: 12px;
                  color: #000000;
                  vertical-align: middle;"
                  >鲁艳洪222</span>
                  <span class="address"  style="position: absolute;
                                  font-size: 12px;
                                  top:5px;
                                  right: -110px;
                                  color: #857e76;
                                  vertical-align: middle;
                                  max-width: 12em;
                                  overflow: hidden;
                                  white-space: nowrap;
                                  text-overflow: ellipsis;">上海 闲时蜗居云南菜</span></p>
              </div>

              <div class="swiper-slide">
                <img style="width:324px;height: 139px;margin-top: -1px;" src="./images/111.jpg" />
                <p
                  style="font-size:18px;margin-left: -38px;margin-top: -48px;color:#fff"
                >2分钟原料验收科普小剧场</p>
                <p style="margin-left: -38px;margin-top: 30px;">管好这6大环节，食材验收不出错</p>
              </div>
              <div class="swiper-slide">
                <img style="width:324px;height: 139px;margin-top: -1px;" src="./images/111.jpg" />
                <p
                  style="font-size:18px;margin-left: -38px;margin-top: -48px;color:#fff"
                >2分钟原料验收科普小剧场</p>
                <p style="margin-left: -38px;margin-top: 30px;">管好这6大环节，食材验收不出错</p>
              </div>
              <div class="swiper-slide">
                <img style="width:324px;height: 139px;margin-top: -1px;" src="./images/111.jpg" />
                <p
                  style="font-size:18px;margin-left: -38px;margin-top: -48px;color:#fff"
                >2分钟原料验收科普小剧场</p>
                <p style="margin-left: -38px;margin-top: 30px;">管好这6大环节，食材验收不出错</p>
              </div>
             
            </div>
            <!-- Add Pagination -->
            <div class="swiper-pagination"></div>
          </div>
        </div>
      </el-col>
    </el-row>


    <!-- youyicheng -->
      <el-row :gutter="20" >
      <el-col :span="6" >
        <div class="grid-content bg-purple"></div>
      </el-col>
      <el-col :span="12">
        <div class="grid-content bg-purple">
          <img src="./images/22.png" />
          <a>精选专题22</a>
          <img src="./images/11.png" />
        </div>
      </el-col>
     
    </el-row>
    <p style="font-size: 8px;">实用百科 / 行家诀窍 / 食安头条</p>
    <el-row style=" margin-top: 9px;" :gutter="20">
      <el-col :span="12">
        <div class="grid-content bg-purple">
          <a href="#">
            <img style="width:90%;height:60px" src="./images/6.png" />
          </a>
        </div>
      </el-col>
      <el-col :span="12">
        <div class="grid-content bg-purple">
          <a href="#">
            <img style="width:90%;height:60px" src="./images/7.png" />
          </a>
        </div>
      </el-col>
    </el-row>
    <el-row style=" margin-top: -15px;" :gutter="20">
      <el-col :span="12">
        <div class="grid-content bg-purple">
          <a href="#">
            <img style="width:90%;height:60px" src="./images/6.png" />
          </a>
        </div>
      </el-col>
      <el-col :span="12">
        <div class="grid-content bg-purple">
          <a href="#">
            <img style="width:90%;height:60px" src="./images/7.png" />
          </a>
        </div>
      </el-col>
    </el-row>
  </div>
  
</template>


<script>
import "swiper/dist/css/swiper.css";
import Swiper from "swiper";
import { swiper, swiperSlide } from "vue-awesome-swiper";
export default {
  mounted() {
    this.getswipe();
  },
  components: {
    swiper,
    swiperSlide
  },
  data() {
    return {
      input: "",
      lst: [
        "https://www.unileverfoodsolutions.com.cn/content/ufs/zh/recipes/jjghhzyk/_jcr_content/recipeMain/image.img.jpg/1513762361509.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/ufs/zh/banners/homepageKV2/_jcr_content/banners/banneritem_710086888/image.img.jpg/1564718163062.jpg",
        "https://www.unileverfoodsolutions.com.cn/content/dam/ufs/images/Homepage/kv/%e8%92%9c%e9%a6%99.gif",
        "https://www.unileverfoodsolutions.com.cn/content/ufs/zh/banners/homepageKV2/_jcr_content/banners/banneritem_689493021/image.img.jpg/1561618880431.jpg"
      ]
    };
  },
  methods: {
    getswipe() {
      var swiper = new Swiper(".swiper-container", {
        pagination: ".swiper-pagination",
        slidesPerView: "auto",
        centeredSlides: true,
        paginationClickable: true,
        spaceBetween: 30
      });
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
*{
  box-sizing: border-box;
  margin: 0px;
  padding: 0px;
}
#app{
  background-color: #FAF5Ef
}
a {
  text-decoration: none;
}
.abiao {
  display: block;
  font-size: 12px;
  text-align: center;
  font-weight: bold;
  color: rgba(255, 255, 255, 0.7);
  letter-spacing: 0.1em;
  padding: 5px;
  /* width: 22%; rgba(255, 255, 255, 0.2)*/
  border:2px solid rgba(255, 255, 255, 0.2);
  border-radius: 8px;
  border-right-color: transparent;
  border-left-color: transparent;
}
#app {
  margin-top: -8px;
}

/* .el-col2 {
  margin-top: 23px;
} */
.el-icon-s-grid {
  margin-top: 5px;
  margin-right: 20px;
  font-size: 30px;
}

.grid-content bg-purple:nth-child(3) {
  font-size: 30px;
}
.el-row {
  margin-bottom: 20px;
  line-height: 
  &:last-child {
    margin-bottom: 0;
  }
}
.el-col {
  border-radius: 4px;
}
.bg-purple-dark {
 /* 轮播图 background: #99a9bf; */
}
.bg-purple {
}
.bg-purple-light {
  background: #e5e9f2;
}
.grid-content {
  border-radius: 4px;
  min-height: 25px;
}
.row-bg {
  padding: 10px 0;
  background-color: #f9fafc;
}
/* 走马灯 */
.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 100px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}

/*swipet*/
.swiper-container {
  width: 100%;
  height: 250px;
  margin: 20px auto;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: white;
  width: 324px;
  height: 200px;

  /* Center slide text vertically */
  /* display: -webkit-box;
        display: -ms-flexbox;
        display: -webkit-flex; */
  /* display: flex;
        -webkit-box-pack: center;
        -ms-flex-pack: center;
        -webkit-justify-content: center;
        justify-content: center;
        -webkit-box-align: center;
        -ms-flex-align: center;
        -webkit-align-items: center;
        align-items: center; */
}

.swiper-slide:nth-child(2) {
  width: 324px;
  height: 200px;
}
.swiper-slide:nth-child(3n) {
  width: 324px;
  height: 200px;
}
</style>
