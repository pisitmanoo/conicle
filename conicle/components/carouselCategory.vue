<template>
  <div>
    <h1>Category</h1>
    <el-divider />
    <el-carousel interval: arrow="always" height="260px">
      <!-- page -->
      <el-carousel-item v-for="item in 3" :key="item">
        <el-row>
          <!-- box in page -->
          <el-col
            :span="6"
            v-for="(o, index) in 4"
            :key="o"
            :offset="index > 3 ? 2 : 0"
          >
            <el-card class="img">
              <el-row>
              <div class="text-container">
                <img src="../assets/Category1.jpg" class="img"/>
                <div class="centered" >Podcast</div>
                <div class="centered-2" >(12 contents)</div>
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


.text-container {
  position: relative;
  text-align: center;
  color: white;
}

.centered {
  position: absolute;
  top: 45%;
  left: 50%;
  transform: translate(-50%, -50%);
  padding: 0px 0px 10px;
}

.centered-2 {
  position: absolute;
  top: 60%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.img{
    width:100%;
    border-radius: 16px !important;
    border-color: none !important;
    
}
.img::hover{
    background: red;

}
</style>
