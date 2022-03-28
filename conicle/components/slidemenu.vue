<template>
  <div class="container" >
    <el-menu
      class="el-menu-vertical-demo"
      @click="statechange"
      @open="handleOpen"
      @close="handleClose"
      :collapse="isCollapse"
    >
      <el-menu-item index="1" class="el-color-font">
        <i-r class="el-icon-s-home"></i-r>
        <span slot="title">Home</span>
      </el-menu-item>

      <el-menu-item index="2">
        <i class="el-icon-news"></i>
        <span slot="title">New Update</span>
      </el-menu-item>
      <!-- <h2>Explore</h2> -->
      <el-menu-item index="3" class="el-color-font">
        <span slot="title">Explore</span>
      </el-menu-item>
      <el-menu-item index="4">
        <i class="el-icon-eleme"></i>
        <span slot="title">ConicleX Courses</span>
      </el-menu-item>
      <el-menu-item index="5">
        <i class="el-icon-coin"></i>
        <span slot="title">Learning Material</span>
      </el-menu-item>
      <el-menu-item index="6">
        <i class="el-icon-sort"></i>
        <span slot="title">Learning Path</span>
      </el-menu-item>
    </el-menu>
  </div>
</template>


<script>
export default {
  props:{
    isCollapse: Boolean,
  },
  data() {
    return {
      // isCollapse: true,
      
    }
  },
  methods: {
    handleOpen(key, keyPath) {
      console.log(key, keyPath)
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath)
    },
  },
}
</script>


<style>
.el-menu-vertical-demo:not(.el-menu--collapse) {
  width: 100%;
  min-height: 400px;
}

.el-color-font{
  color: #ff0712
}

i-r{
  color:#ff0712
}
</style>