<template>
  <div class="home_body">
    <el-col
      class="allheight adjust_blank"
      :span="3"
      style="border-right: 1px solid rgba(212, 212, 212, 0.1)"
    ></el-col>
    <el-col class="allheight" :span="18">
      <el-row class="main_row_one">
        <!--Logo-->
        <div class="top_col_one">
          <img class="logo" src="../assets/images/king.png" />
          <div class="logo_text">King</div>
        </div>
        <!--导航-->
        <div class="top_col_two">
          <div class="menu_body">
            <div class="menu"><span>Product</span></div>
            <div class="menu"><span>Interest</span></div>
            <div class="menu"><span>Artcles</span></div>
            <div class="menu"><span>Home</span></div>
          </div>
        </div>
      </el-row>
      <el-row class="main_row_two">
        <!--轮播图-->
        <div class="img_swiper">
          <div class="swiper"></div>
          <div class="mask"></div>
        </div>
        <!--文字介绍-->
        <div class="introduct"></div>
      </el-row>
    </el-col>
    <el-col
      class="allheight adjust_blank"
      :span="3"
      style="border-left: 1px solid rgba(212, 212, 212, 0.1)"
    ></el-col>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      activeIndex: "1",
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.home_body {
  height: 100%;
  width: 100%;
  background-color: rgba(0, 0, 0, 0.8);
  position: relative;
}
.allheight {
  height: 100%;
  position: relative;
}
.main_row_one {
  height: 15%;
  width: 100%;
}
.main_row_two {
  height: 85%;
  width: 100%;
  box-sizing: border-box;
  padding: 2%;
  /* background-color: salmon; */
}
.logo {
  width: 45px;
  height: 45px;
  position: relative;
  float: left;
  left: 10%;
  top: 50%;
  opacity: 0.8;
  transform: translateY(-50%);
}
.logo_text {
  position: relative;
  font-size: 25px;
  font-family: fantasy;
  letter-spacing: 3px;
  top: 50%;
  transform: translateY(-40%);
  color: rgba(255, 255, 255, 0.7);
  font-weight: 200;
  float: left;
  left: 18%;
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
  color: rgba(255, 255, 255, 0.5);
  position: relative;
  top: 50%;
  transform: translateY(-50%);
  height: 100%;
  width: 10%;
  margin: 0 10px;
  padding: 0;
  display: inline;
  float: right;
}
.menu :hover {
  color: rgba(255, 72, 72, 0.8);
  cursor: pointer;
}
.img_swiper {
  width: 80%;
  height: 100%;
  position: relative;
  box-sizing: border-box;
}
.swiper {
  position: relative;
  float: left;
  width: 80%;
  height: 100%;
  background-color: silver;
}
.mask{
  position: relative;
  float: left;
  width: 20%;
  height: 100%;
  background-color: rgba(80, 80, 80, 0.3);
}
</style>
<style>
</style>

