<template>
  <div>
    <el-carousel :interval="4000" type="card"  >
      <el-carousel-item  v-for="item in images" :key="item.id">
        <img
          class="image"
          :src="require(`../assets/${item.image}`)"
          :alt="item.image"
        />
      </el-carousel-item>
    </el-carousel>
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: [
        {
          id: 1,
          image: 'top1.png',
        },
        {
          id: 2,
          image: 'top2.jpg',
        },
        {
          id: 3,
          image: 'top3.png',
        },
        {
          id: 4,
          image: 'top4.png',
        },
        {
          id: 5,
          image: 'top5.png',
        },
        {
          id: 6,
          image: 'top6.png',
        },
        {
          id: 7,
          image: 'top7.png',
        },
      ],
    }
  },
  method() {},
}
</script>
>

<style>
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

.image {
  max-width: 800;
  max-height: 448;
  width: 100%;
  height: 100%;
}
</style>
