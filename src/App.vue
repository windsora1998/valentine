<template>
  <ValentineCard/>
</template>

<script>
import ValentineCard from './components/ValentineCard.vue'

export default {
  name: 'App',
  components: {
    ValentineCard
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

@import url('https://fonts.googleapis.com/css2?family=Pacifico&display=swap');

body {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #ff758f;
}
</style>
