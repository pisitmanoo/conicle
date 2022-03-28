<template>
  <div class="container">
    <el-row type=flex class="container-footer-top">
      <el-row class="footer-information">
        <el-col :span="11">
          <img
            class="logo-foot"
            :src="require(`../assets/${footer_img}`)"
            :alt="footer_img"
          />
          <h4>
            ConicleX - Professional Lifelong Learning
            แหล่งรวมการเรียนรู้ออนไลน์ที่ดีที่สุดสำหรับ Professional
            เปิดให้คุณได้ Upskill / Reskill ในทักษะแห่งศตวรรษที่ 21 (21st
            Century Skills) ให้พร้อมก้าวกระโดดในการทำงานแห่งอนาคต
          </h4>
          <h4>
            - สนใจคอร์สเรียนบน coniclex.com แบบออกใบกำกับภาษี ติดต่อ คุณบอลล์
            061-669-6366 - สนใจคอร์สเรียนแพ็กเกจสำหรับองค์กร
            business.coniclex.com ติดต่อ คุณตี๋ 090-995-6246 เวลาทำการ
            จันทร์-ศุกร์ 09:00 - 18:00 น.
            <el-button type="text" class="btn container">See More</el-button>
          </h4>
        </el-col>
        <el-col :span="5"><div class="grid-content-white"></div></el-col>
        <el-col :span="3">
          <el-link type="text" :underline="false">Terms & Conditions</el-link>
        </el-col>
        <el-col :span="2">
          <el-link type="text" :underline="false" >Contact Us</el-link>
        </el-col>
        <el-col :span="3">
          <el-link type="text" :underline="false"
            >ConicleX for Business</el-link
          >
        </el-col>
      </el-row>
    </el-row>

    <el-divider />
    <el-row :gutter="20" class="container-footer-under">
      <el-col :span="12">
        Copyright © 2021 Conicle Co., Ltd. All rights reserved for all contents.
        | Current version 4.9.446
      </el-col>
      <el-col :span="8"><div class="grid-content-white"></div></el-col>
      <el-col :span="4" class="btn-and-link">
        Powered by
        <img
          class="logo-small"
          :src="require(`../assets/${footer_img}`)"
          :alt="footer_img"
        />
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      footer_img: 'conicle_footer.png',
    }
  },
}
</script>

<style scoped>
.container {
  background: #ff0712;
  color: #ffffff;
}

.btn {
  margin-left: 50%;
  margin-right: 50%;
}
.logo-foot {
  max-width: 112.77px;
  max-height: 47px;
}
.logo-small {
  max-height: 21px;
}

.container-footer-top {
  margin: 80px 0px 0px;
  padding: 0px 150px;
}

.container-footer-under {
  padding: 0px 150px;
}

.footer-information {
  padding: 45px 0px 0px;
}

.grid-content-blank {
  background: whie;
  border-radius: 4px;
  min-height: 36px;
}

.btn-and-link{
  padding-left: 50%;
  padding-right: 50%;
}
</style>
