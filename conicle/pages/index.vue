<template>
  <div>
    <headerbar />
    <el-row >
      <!-- <el-col :span="6"> <Header /></el-col> -->
      <el-col >
        <CarouselTop />
        <CarouselLearning />
        <CarouselCategory />
        <Footer/></el-col>

      
    </el-row>
    <!-- <el-container>
  <el-header><headerbar /></el-header>
  <el-container>
    <el-aside ><Header /></el-aside>
    <el-container>
      <el-main><CarouselTop /></el-main>
      <el-main><CarouselLearning /></el-main>
      <el-main><CarouselCategory /></el-main>
      <el-footer><Footer/></el-footer>
    </el-container>
  </el-container>
</el-container> -->
  </div>
</template>

<script>
import CarouselTop from '../components/carouselTop.vue'
import CarouselLearning from '../components/carouselLearning.vue'
import CarouselCategory from '../components/carouselCategory.vue'
import Footer from '../components/footer.vue'
import Header from '../components/header.vue'
import Headerbar from '../components/headerbar.vue'

export default {
  name: 'IndexPage',
  components: {
    CarouselTop,
    CarouselLearning,
    CarouselCategory,
    Footer,
    Header,
    Headerbar,
  },
}
</script>

<style>
  .el-header, .el-footer {
    background-color: #B3C0D1;
    color: #333;
    text-align: center;
    line-height: 60px;
  }
  
  .el-aside {
    background-color: #D3DCE6;
    color: #333;
    text-align: center;
    line-height: 200px;
  }
  
  .el-main {
    background-color: #E9EEF3;
    color: #333;
    text-align: center;
    line-height: 160px;
  }
  
  body > .el-container {
    margin-bottom: 40px;
  }
  
  .el-container:nth-child(5) .el-aside,
  .el-container:nth-child(6) .el-aside {
    line-height: 260px;
  }
  
  .el-container:nth-child(7) .el-aside {
    line-height: 320px;
  }
</style>