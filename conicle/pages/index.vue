<template>
  <div >
    <headerbar @slidemenu="slidemenu" />
    <div style="display:flex">
      <div > <Slidemenu :isCollapse="isCollapse"/></div>
      <div>
        <CarouselTop />
        <CarouselLearning />
        <CarouselCategory />
        <Footer
      /></div>
    </div>
    
  
    <!-- <el-row :gutter="20">
      <el-col type="flex" :span="24"><headerbar @slidemenu="slidemenu" />
      </el-col>
    </el-row >
    <el-row type="flex" :gutter="20">
      <el-col :span="4"> <Slidemenu :isCollapse="isCollapse"/></el-col>
      <el-col  :span="20" type="flex">
        <CarouselTop />
        <CarouselLearning />
        <CarouselCategory />
        <Footer
      /></el-col>
    </el-row> -->
    
    
    
  






  </div>

  



</template>

<script>
import CarouselTop from '../components/carouselTop.vue'
import CarouselLearning from '../components/carouselLearning.vue'
import CarouselCategory from '../components/carouselCategory.vue'
import Footer from '../components/footer.vue'
import Slidemenu from '../components/slidemenu.vue'
import Headerbar from '../components/headerbar.vue'

export default {
  name: 'IndexPage',
  components: {
    CarouselTop,
    CarouselLearning,
    CarouselCategory,
    Footer,
    Slidemenu,
    Headerbar,
  },
  data() {
    return {
      isCollapse: true,
    }
  },
  methods:{
    slidemenu(value){
      this.isCollapse=value
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Kanit:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

*{
  font-family: 'Kanit';
}

.el-header,
.el-footer {
  background-color: #b3c0d1;
  color: #333;
  text-align: center;
  line-height: 60px;
}

.el-aside {
  background-color: #d3dce6;
  color: #333;
  text-align: center;
  line-height: 200px;
}

.el-main {
  background-color: #e9eef3;
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

.weight-components{
  weight:100%
}
</style>
