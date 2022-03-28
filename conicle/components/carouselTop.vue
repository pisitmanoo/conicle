<template>
  <div >
    <el-carousel :interval="4000" type="card" class="img-box" height="500px">
      <el-carousel-item  v-for="item in images" :key="item.id">
        <img
          class="image img-box"
          :src="require(`../assets/${item.image}`)"
          :alt="item.image"
          :span="4"
          :offset="4"
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



.image {
  max-width: 800;
  max-height: 448;
  width: 100%;
  height: 100%;
}
.img-box{
  border-radius: 16px !important;
  border-color: none  !important;
}

</style>
