<template>
  <div>
    <h1>Editor's Pick Online Learning Path</h1>
    <el-divider />
    <el-carousel trigger="click" arrow="always" height="400px">
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
                <img v-for="item in images" :key="item.id" :src="require(`../assets/${item.image}`)" class="image" />
                
                <div>
                <span>เทคนิคการนำเสนอ</span>
                  <h5 class="sub-title-form"
                    >Ways to Become a Better Presenter - เพิ่มทักษะการนำเสนองาน
                    สะกดคนฟังให้สนใจ ด้วย 4 คอร์ส จาก 4 ผู้เชี่ยวชาญ </h5
                  >
                  <!-- ทั้ง
                    แอดทอย-กษิดิศ สตางค์มงคล ผู้เชี่ยวชาญด้าน Data Analytics
                    เจ้าของเพจ DataRockie อาจารย์ต้องตา-พญ.สุธาพร ล้ำเลิศกุล
                    วิทยากรผู้เชี่ยวชาญด้านการนำเสนอและ Visual Presentation จาก
                    BetterPitch คุณฝ้าย-เอมิสา รักสยาม
                    วิทยากรผู้เชี่ยวชาญด้านการพัฒนาบุคลิกภาพและภาพลักษณ์ จาก
                    IDEO Empowerment และคุณเฟิน-ปณิชา ชาญฤทธิเสน Managing
                    Director จาก K Innovation วิทยากรผู้เชี่ยวชาญด้านการสื่อสาร
                    จาก IDEO Empowerment ให้ผู้เรียนสามารถออกแบบ Presentation
                    ได้เหนือชั้น เพิ่มประสิทธิภาพการนำเสนองาน
                    และสร้างความประทับใจให้ผู้ฟังได้สำเร็จ -->
                  <el-row :gutter="20">
                    <el-col :span="10"> conicle </el-col>
                    <el-col :span="10">2599</el-col>
                  </el-row>
                  <el-divider />
                  <el-row :span="2">5 hrs</el-row>
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
      currentDate: new Date(),
      images: [
        {
          id: 0,
          image: ['Learn1.jpg'],
        },
        
      ],
    }
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
}

.clearfix:before,
.clearfix:after {
  display: table;
  content: '';
}

.clearfix:after {
  clear: both;
}

.el-carousel__item h3 {
  color: #475669;
  font-size: 18px;
  opacity: 0.75;
  line-height: 300px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}

.sub-title-form{
    color:gray;
    padding: 12px
}

</style>
