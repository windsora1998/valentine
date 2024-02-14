<template>
  <div class="top-card">
    <ValentineCard />
  </div>
  <div class="top-scroll flex items-center justify-center">
    <ValentineSroll />
  </div>
  <div class="title-gallery">Our Gallery</div>
  <div class="mb-[48px] grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-10 md:ml-6 md:mr-6 lg:mr-8 lg:ml-8">
    <div v-for="item in lstNumber" :key="item">
      <CardImage :key="item" :date="item.date" :content="item.content"  :url="`/valentine/image/${item.id}.jpeg`" />
    </div>
  </div>
</template>

<script>


import ValentineCard from "./components/ValentineCard.vue";
import ValentineSroll from "./components/ValentineSroll.vue";
import CardImage from "./components/CardImage.vue";


export default {
  name: "App",
  components: {
    ValentineCard,
    ValentineSroll,
    CardImage,
  },
  data: function () {
    return {
      lstNumber:  [{
        id: 2,
        date: '8/12/2023',
        content: 'Người yêu tôi tấm này xinh quá!'
      },
      {
        id: 3,
        date: '19/12/2023',
        content: 'Hồi ức khuyên mũi'
      },
      {
        id: 4,
        date: '21/12/2023',
        content: 'Dám chụp lén người yêu'
      },
      {
        id: 5,
        date: '21/12/2023',
        content: 'Giả bộ bồng cháu đồ :)))'
      },
      {
        id: 6,
        date: '25/12/2023',
        content: 'Checkin Hội An. Nguyên ngày dụ dỗ người ta đi Hội An'
      },
      {
        id: 7,
        date: '25/12/2023',
        content: 'Lần đầu tiên được ăn noel với người yêu'
      },
      {
        id: 8,
        date: '25/12/2023',
        content: 'Nguyên một bàn tiệc xịn sò'
      },
      {
        id: 9,
        date: '26/12/2023',
        content: 'Che dữ chưa'
      },
      {
        id: 10,
        date: '26/12/2023',
        content: 'Chụp chục tấm mãi được một tấm dễ thương'
      },
      {
        id: 11,
        date: '27/12/2023',
        content: 'Chu mỏ đồ'
      },
      {
        id: 12,
        date: '27/12/2023',
        content: 'Nghiêm túc quá không quen'
      },
      {
        id: 13,
        date: '1/1/2024',
        content: 'Bánh bao bị bóp rồi'
      }
    ],
    };
  },
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: auto;
}

@import url("https://fonts.googleapis.com/css2?family=Pacifico&display=swap");

.top-card {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #ff758f;
}

.top-scroll {
  margin-top: 48px;
}

.gallery {
  display: flex;
  align-items: center;
  justify-content: center;
  height: auto;
  background-color: #ff758f;
}

.title-gallery {
  color: #830d2e;
  font-size: 60px;
  font-family: "Pacifico", cursive;
  line-height: 1;
  text-align: center;
  z-index: 3;
  animation: up 1s ease forwards;
  transition: 0.2s;
  padding: 128px 0px;
  margin: 48px 0;
  background-color: #ebcbd2;
}
</style>
