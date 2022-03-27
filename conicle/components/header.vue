<template>
  <div class="container" >
    <el-menu
      default-active="2"
      class="el-menu-vertical-demo"
      @click="statechange"
      @open="handleOpen"
      @close="handleClose"
      :collapse="isCollapse"
    >
      <el-menu-item index="1">
        <i class="el-icon-menu"></i>
        <span slot="title">Home</span>
      </el-menu-item>

      <el-menu-item index="2">
        <i class="el-icon-setting"></i>
        <span slot="title">New Update</span>
      </el-menu-item>
      <!-- <h2>Explore</h2> -->
      <el-menu-item index="3">
        <i class="el-icon-menu"></i>
        <span slot="title">Explore</span>
      </el-menu-item>
      <el-menu-item index="4">
        <i class="el-icon-menu"></i>
        <span slot="title">Explore</span>
      </el-menu-item>
      <el-menu-item index="5">
        <i class="el-icon-menu"></i>
        <span slot="title">Explore</span>
      </el-menu-item>
    </el-menu>
  </div>
</template>

<style>
.el-menu-vertical-demo:not(.el-menu--collapse) {
  width: 200px;
  min-height: 400px;
}
</style>

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
