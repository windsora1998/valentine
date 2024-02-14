<template>
  <div class="top-card">
    <ValentineCard/>
  </div>
  <div class="top-scroll">
    <ValentineSroll/>
  </div>
</template>

<script>
import ValentineCard from './components/ValentineCard.vue'
import ValentineSroll from './components/ValentineSroll.vue'

export default {
  name: 'App',
  components: {
    ValentineCard,
    ValentineSroll
  }
}
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
}

@import url('https://fonts.googleapis.com/css2?family=Pacifico&display=swap');

.top-card {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #ff758f;
}

.top-scroll {
  margin-top: 48px;
  height: 30vh;
}
</style>
