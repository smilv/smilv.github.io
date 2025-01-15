<script setup lang="ts">
defineOptions({ name: "Index" });
const cardList = [
  {
    title: "画板",
    description: "一个简单的画板，可以用来画画。",
    image: "drawing_board.png",
  },
  {
    title: "计算器",
    description: "一个简单的计算器，可以用来计算。",
    image: "calculator.png",
  },
  {
    title: "3D翻转日历",
    description: "一个简单的3D翻转日历，可以用来查看日期。",
    image: "calendar.png",
  },
];
</script>
<template>
  <div class="w-80 h-80 text-9xl p-4 bg-green-800 content-center text-center font-bold">Sm</div>
  <div class="parallax">
    <div class="bg bg_1">
      <div class="sprite"></div>
      <div class="screen">
        <div class="content">
          <h1>Welcome<br />friend</h1>
          <h2>smilv site</h2>
          <p class="bodytext">
            hi, <br />
            this is my personal GitHub site <br />which showcases some projects and fun things. Welcome to explore.
          </p>
        </div>
      </div>
    </div>
    <div class="bg bg_2">
      <div class="sprite"></div>
      <div class="screen"></div>
    </div>
    <div class="bg bg_3">
      <div class="sprite"></div>
      <div class="screen"></div>
    </div>
    <div class="bg bg_4">
      <div class="sprite"></div>
      <div class="screen"></div>
    </div>
  </div>
  <div class="bg-grid">
    <div class="card" v-for="item in cardList">
      <div>
        <a href=""></a>
        <img :src="`/images/card/${item.image}`" alt="" />
        <div class="p-4">
          <div class="title">{{ item.title }}</div>
          <p class="description">{{ item.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
@import "@/assets/css/parallax.scss";
.bg-grid {
  padding: 10px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  background: #f5f5f5;
}
.card {
  background: #fff;
  margin: 5px;
  border: 1px solid #e7e8eb;
  border-radius: 10px;
  text-align: center;
  position: relative;
  transition: all 0.3s;
  bottom: 0;
  overflow: hidden;
  width: 100%;
  &:hover {
    bottom: 8px;
    box-shadow: 0px 0px 12px rgba(0, 0, 0, 0.12);
  }
  img {
    display: block;
    object-fit: cover;
    height: 320px;
    margin: 0 auto;
  }
  .title {
    font-size: 21px;
    font-weight: 400;
    line-height: 1.25;
    font-weight: 500;
  }
  .description {
    margin-top: 0.5rem;
    color: #64748b;
  }
  a {
    position: absolute;
    left: 0;
    top: 0;
    right: 0;
    bottom: 0;
  }
}
@media (min-width: 640px) {
  .card {
    width: calc(50% - 10px);
  }
}

@media (min-width: 1024px) {
  .card {
    width: calc(33.33% - 10px);
  }
}
@media (min-width: 1920px) {
  .card {
    width: calc(25% - 10px);
  }
}
</style>
