<template>
  <svg viewBox="0 0 100 100" width="400" height="400">
    <defs>
      <!-- cloud -->
      <path id="cloud" d="M -15 0 h 30 a 10 10 0 0 0 -10 -10 q -4 0 -8 4 t -8 0 a 8 8 0 0 0 -8 0 q -4 3 -3 6 h 7"
        fill="hsl(40, 85%, 70%)" stroke="hsl(40, 85%, 70%)" stroke-width="1" stroke-linecap="round"
        stroke-linejoin="round"></path>
    </defs>
    <!-- clouds -->
    <g class="clouds" transform="translate(0 0)">
      <use href="#cloud" x="0" y="0" transform="translate(25 30)"></use>
      <use href="#cloud" x="0" y="0" transform="translate(-75 30)"></use>
    </g>
    <!-- wrap the second cloud in a group flipping the shape around the y axis to translate the clouds in the opposite direction -->
    <g transform="translate(75 0) scale(-1 1)">
      <g class="clouds" transform="translate(0 0)">
        <use href="#cloud" x="0" y="0" transform="translate(0 70)"></use>
        <use href="#cloud" x="0" y="0" transform="translate(-100 70)"></use>
      </g>
    </g>
    <!-- arrow -->
    <g transform="translate(50 1)">
      <g class="arrow">
        <!-- heart -->
        <path d="M 0 84 a 6 6 0 0 1 12 0 q 0 6 -12 14 q -12 -8 -12 -14 a 6 6 0 0 1 12 0" fill="hsl(15, 100%, 60%)"
          stroke="hsl(15, 100%, 60%)" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"></path>
        <!-- feather -->
        <path d="M 0 5 l 9 -5 v 22 l -9 5 l -9 -5 v -22 l 9 5" fill="hsl(40, 85%, 70%)" stroke="hsl(40, 85%, 70%)"
          stroke-width="1" stroke-linecap="round" stroke-linejoin="round"></path>
        <path d="M 0 5 l 9 -5 v 6 l -9 5 v 1 l 9 -2 v 12 l -9 5 l -9 -5 v -4 l 9 5 v -1 l -9 -8 v -14 l 9 5"
          fill="hsl(15, 100%, 60%)" stroke="hsl(15, 100%, 60%)" stroke-width="1" stroke-linecap="round"
          stroke-linejoin="round"></path>
        <!-- connecting line -->
        <path d="M 0 5 v 80" fill="none" stroke="hsl(25, 85%, 15%)" stroke-width="1" stroke-linecap="square"></path>
      </g>
    </g>
  </svg>
</template>

<script>
export default {
  name: 'ValentineSroll',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.clouds {
  animation: translateHorizontally 10s cubic-bezier(0.445, 0.3, 0.55, 0.7) infinite;
}

@keyframes translateHorizontally {
  to {
    transform: translateX(100px);
  }
}

.arrow {
  animation: translateVertically 5s cubic-bezier(0.19, 1, 0.22, 1) infinite;
}

/* use opposite timing function as the arrow moves into view and out of sight */
@keyframes translateVertically {
  0% {
    transform: translateY(-100px);
  }

  40% {
    transform: translateY(0px);
    animation-timing-function: cubic-bezier(0.19, 1, 0.22, 1);
  }

  60% {
    transform: translateY(0px);
    animation-timing-function: cubic-bezier(0.895, 0.03, 0.685, 0.22);
  }

  100% {
    transform: translateY(100px);
  }
}</style>
