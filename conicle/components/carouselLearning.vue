<template>
  <div>
    <h1>Editor's Pick Online Learning Path</h1>
    <el-divider />
    <el-carousel trigger="click" arrow="always" height="500px">
      <el-carousel-item v-for="item in 3" :key="item">
        <el-row>
          <el-col
            :span="6"
            v-for="(o, index) in 4"
            :key="o"
            :offset="index > 3 ? 2 : 0"
            
          >
            <el-card
              class="card-box"
              shadow="hover"
            >
              <el-row>
                <img
                  v-for="item in images"
                  :key="item.id"
                  :src="require(`../assets/${item.image}`)"
                  class="image"
                />
                <el-button size="small" class="font-top-left"
                  >OPEN ENROLLMENT</el-button
                >
                <div>
                  <div class="font-section">
                    <span style="color: #b8bfcb"
                      ><i class="el-icon-sort font-l-sec">Learning Path</i
                      ><i class="el-icon-info font-l-sec-2"
                        >Self Development</i
                      ></span
                    >
                  </div>
                  <el-row :span="6" class="font-section">
                    <span>เทคนิคการนำเสนองานระดับมืออาชีพ</span>
                  </el-row>
                  <el-row :span="6" class="sub-title-form">
                    Ways to Become a Better Presenter - เพิ่มทักษะการนำเสนองาน
                    สะกดคนฟังให้สนใจ ด้วย 4 คอร์ส จาก 4 ผู้เชี่ยวชาญ
                  </el-row>
                  <el-row :gutter="20">
                    <el-col type="flex" :span="8" class="font-card"
                      >Conicle Co., Ltd.</el-col
                    >
                    <el-col :span="10"
                      ><div class="grid-content-white"></div
                    ></el-col>
                    <el-col :span="6" class="font-card"
                      ><div>฿2599</div></el-col
                    >
                  </el-row>
                  <el-divider />
                  <el-row :span="6"
                    ><i class="el-icon-time"></i
                    ><span class="font-l-sec-3">5 hrs 5 mins</span></el-row
                  >
                </div>
              </el-row>
            </el-card>
          </el-col>
        </el-row>
      </el-carousel-item>
    </el-carousel>
    <el-divider />
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
      currentDate: new Date(),
      images: [
        {
          id: 1,
          image: 'Learn1.jpg',
        },
        // {
        //   id: 1,
        //   image: 'Learn2.jpg',
        // },
      ],
    }
  },
  methods: {
    plusCount() {
      this.count += 1
    },
  },
}
</script>

<style>
.time {
  font-size: 13px;
  color: #999;
}

.bottom {
  margin-top: 13px;
  line-height: 12px;
}

.button {
  padding: 0;
  float: right;
}

.image {
  width: 100%;
  height: 100%;
  display: block;
  border-radius: 16px 16px 0px 0px !important;
}

.clearfix:before,
.clearfix:after {
  display: table;
  content: '';
}

.clearfix:after {
  clear: both;
}



.card-box {
  margin: 5px;
  border-radius: 16px !important;
  border-color: none !important;
  padding: 0px; 
  height: 480px;  /* width: 21%; */
  box-shadow: gray;
}

.sub-title-form {
  color: gray;
  font-size: 12px;
  margin: 4px 0px;
  /* padding: 0px 4px 4px; */
}

.font-top-left {
  background: white;
  color: #1e88e5;
  padding: 4px 8px;
  position: absolute;
  top: 8px;
  left: 16px;
  font-size: 16px;
}

.font-under-title {
  font-size: 12px;
}

.font-size-section {
  margin-left: 16px;
  font-size: 16px;
}
.font-l-sec {
  color: #5f25bd;
}

.font-l-sec-2 {
  margin-left: 5px;
  color: #b8bfcb;
  font-size: 12px;
}
.font-l-sec-3 {
  color: black;
  margin-left: 5px;
}

.grid-content-white {
  background: whie;
  border-radius: 4px;
  min-height: 36px;
}
</style>
