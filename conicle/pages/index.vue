<template>
  <div >
    <headerbar @slidemenu="slidemenu" />
    <div style="display:flex">
      <div :span="6"> <Header :isCollapse="isCollapse"/></div>
      <div>
        <CarouselTop />
        <CarouselLearning />
        <CarouselCategory />
        <Footer
      /></div>
    </div>
    
    
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
</style>
