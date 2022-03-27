<template>
  <div>
    <h1>Category</h1>
    <el-divider />
    <!-- <div class="container">
      <img
        src="../assets/Category1.jpg"
      class="img"/>

      <div class="centered" >Centered</div>
    </div> -->

    <el-carousel interval: arrow="always" height="400px">
      <el-carousel-item v-for="item in 3" :key="item">
        <el-row>
          <el-col
            :span="6"
            v-for="(o, index) in 4"
            :key="o"
            :offset="index > 3 ? 2 : 0"
            
          >
            <el-card :body-style="{ padding: '0px' }">
              <el-row>
                <div class="container">
      <img
        src="../assets/Category1.jpg"
      class="img"/>

      <div class="centered" >Centered</div>
    </div>
                
              </el-row>
            </el-card>
          </el-col>
        </el-row>
      </el-carousel-item>
    </el-carousel>
  </div>
</template>

<style scoped>

.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 200px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}

.container {
  position: relative;
  text-align: center;
  color: white;
}

.centered {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.img{
    width:100%
}
.img::hover{
    background: red;
}
</style>
