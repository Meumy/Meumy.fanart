<template>
  <div class="home_body">
    <!-- <canvas id='canvas'></canvas> -->
    <el-col class="allheight adjust_blank" :span="3"></el-col>
    <el-col class="allheight" :span="18">
      <el-row class="main_row_one">
        <!--Logo-->
        <div class="top_col_one">
          <img class="logo" src="../assets/images/king.png" />
          <div class="logo_text">
              <span>K</span>
              <span>i</span>
              <span>n</span>
              <span>g</span>
          </div>
        </div>
        <!--导航-->
        <div class="top_col_two">
          <div class="menu_body">
            <span class="menu style_prevu_kit" id="performance">Works</span>
            <span class="menu style_prevu_kit" id="Interest">Interest</span>
            <span class="menu style_prevu_kit" id="Artcles">Artcles</span>
            <span class="menu active style_prevu_kit" id="Home">Home</span>
          </div>
        </div>
      </el-row>
      <el-row class="main_row_two">
        <!--轮播图-->
        <div class="img_swiper">
          <div class="swipering">
            <swiper ref="mySwiper" :options="swiperOption">
              <swiper-slide
                ><img class="imgadjust" src="../assets/images/swiper_1.jpg"
              /></swiper-slide>
              <swiper-slide
                ><img class="imgadjust" src="../assets/images/swiper_2.jpg"
              /></swiper-slide>
              <swiper-slide
                ><img class="imgadjust" src="../assets/images/swiper_3.jpg"
              /></swiper-slide>
              <swiper-slide
                ><img class="imgadjust" src="../assets/images/swiper_4.jpg"
              /></swiper-slide>
              <swiper-slide
                ><img class="imgadjust" src="../assets/images/swiper_5.jpg"
              /></swiper-slide>
              <swiper-slide
                ><img class="imgadjust" src="../assets/images/swiper_6.jpg"
              /></swiper-slide>
              <div class="swiper-pagination" slot="pagination"></div>
            </swiper>
          </div>
          <div class="mask"></div>
        </div>
        <!--文字介绍-->
        <div class="introduct">
          <div class="name">
            <span class="title">King.Jin</span>
          </div>
          <div class="address">
            <span class="subtitle">ZheJiang , China</span>
          </div>
          <div class="text">
            <span
              >A sunny and handsome boy in China.Like reading, playing chess,
              playing games, love the two-dimensional culture and Vtubers</span
            >
          </div>
        </div>
      </el-row>
    </el-col>
    <el-col class="allheight adjust_blank" :span="3"></el-col>
  </div>
</template>

<script>
import "swiper/dist/css/swiper.css";
import { Swiper, SwiperSlide, directive } from "vue-awesome-swiper";
import '../common/canvas.js'
export default {
  name: "Home",
  components: {
    Swiper,
    SwiperSlide,
  },
  directives: {
    swiper: directive,
  },
  data() {
    return {
      activeIndex: "1",
      swiperOption: {
        spaceBetween: 10,
        loop: true,
        autoplay: 3000,
        autoplayDisableOnInteraction: false,
        pagination: {
          el: ".swiper-pagination",
          type: "fraction",
        },
      },
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import "../common/Home.css";
@import "../common/textjump.css";
@import "../common/canvas.css";

.home_body {
  height: 100%;
  width: 100%;
  /* background-color: rgba(0, 0, 0, 0.8); */
  position: relative;
}
.allheight {
  height: 100%;
  position: relative;
}
.main_row_one {
  height: 20%;
  width: 100%;
}
.main_row_two {
  height: 80%;
  width: 100%;
  box-sizing: border-box;
  padding-left: 1%;
  /* background-color: salmon; */
}
.logo {
  width: 60px;
  height: 60px;
  position: relative;
  float: left;
  left: 10%;
  top: 50%;
  opacity: 0.8;
  transform: translateY(-50%);
}
.logo_text {
  position: absolute;
  font-size: 32px;
  font-family: fantasy;
  letter-spacing: 3px;
  top: 45%;
  transform: translateY(-40%);
  color: rgba(255, 255, 255, 0.7);
  font-weight: 200;
  float: left;
  left: 35%;
}
.top_col_one {
  height: 100%;
  width: 25%;
  position: relative;
  display: inline-block;
  float: left;
}
.top_col_two {
  height: 100%;
  width: 75%;
  position: relative;
  display: inline-block;
  padding-right: 2%;
  float: right;
  box-sizing: border-box;
}
span {
  position: relative;
  top: 50%;
  transform: translateY(-50%);
}
.menu_body {
  height: 50%;
  width: 95%;
  position: relative;
  margin-right: 2%;
  top: 50%;
  transform: translateY(-50%);
}
.menu {
  color: rgba(255, 255, 255, 0.7);
  position: relative;
  top: 50%;
  transform: translateY(-50%);
  background-color: rgba(240, 0, 0, 0);
  margin: 0 20px;
  padding: 0;
  display: inline;
  float: right;
  font-size: 20px;
}
.menu :hover {
  color: rgba(255, 72, 72, 0.8);
  cursor: pointer;
}
.active {
  color: rgba(255, 72, 72, 0.8);
}
.img_swiper {
  width: 84%;
  height: 100%;
  position: relative;
  box-sizing: border-box;
}
.swipering {
  position: relative;
  float: left;
  width: 72%;
  height: 100%;
  /* background-color: silver; */
}
.swiper-container,
.swiper-wrapper,
.swiper-slide {
  height: 100%;
  width: 100%;
  position: relative;
}
.mask {
  position: relative;
  float: left;
  width: 28%;
  height: 73.6%;
  top: 40%;
  left: 5%;
  transform: translateY(-50%);
  background-color: rgba(71, 71, 71, 0.3);
}
.introduct {
  float: right;
  position: absolute;
  top: 0;
  right: 0;
  width: 32%;
  height: 100%;
}
.name,
.address,
.text {
  float: right;
  text-align: left;
  position: relative;
  margin-top: 40%;
  width: 100%;
  height: max-content;
}
.address {
  margin-top: 3%;
}
.text {
  margin-top: 4%;
  padding-right: 8%;
  text-align: inter-word;
  word-break: break-all;
  box-sizing: border-box;
  font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
    "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
  font-size: 16px;
  color: rgba(255, 255, 255, 0.5);
}
.title {
  font-size: 50px;
  font-family: Georgia, "Times New Roman", Times, serif;
  letter-spacing: 2px;
  color: rgba(252, 86, 86, 0.6);
}
.subtitle {
  font-size: 18px;
  margin-left: 2%;
  letter-spacing: 2px;
  font-family: Georgia, "Times New Roman", Times, serif;
  color: rgba(255, 255, 255, 0.8);
}
.text span {
  margin-left: 2%;
  width: 100%;
}
.imgadjust {
  width: 100%;
  position: relative;
  top: 40%;
  transform: translateY(-50%);
}
.swiper-pagination {
  width: 100%;
  height: 10px;
}
</style>
<style>
</style>

