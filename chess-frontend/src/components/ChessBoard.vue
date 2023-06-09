<script setup>
  // import { ref } from 'vue';
  const highlightSquare = (e) => {
    const clickedSquare = e.target
    // only target children
    if (clickedSquare.classList.contains('square')) {
      // toggle highlighted colour
      clickedSquare.classList.toggle('highlighted')
    }
  }

//   const squares = ref([
//   'dark', 'light', 'dark', 'light', 'dark', 'light', 'dark', 'light',
//   'light', 'dark', 'light', 'dark', 'light', 'dark', 'light', 'dark',
//   'dark', 'light', 'dark', 'light', 'dark', 'light', 'dark', 'light',
//   'light', 'dark', 'light', 'dark', 'light', 'dark', 'light', 'dark',
//   'dark', 'light', 'dark', 'light', 'dark', 'light', 'dark', 'light',
//   'light', 'dark', 'light', 'dark', 'light', 'dark', 'light', 'dark',
//   'dark', 'light', 'dark', 'light', 'dark', 'light', 'dark', 'light',
//   'light', 'dark', 'light', 'dark', 'light', 'dark', 'light', 'dark'
// ]);
</script>

<template>
    <!-- <div class="board" @click="highlightSquare">
    <div
      v-for="(square, index) in squares"
      :key="index"
      :class="[square, { 'highlight': square === 'clicked' }]"
    ></div>
  </div> -->
  <div class="board" @click="highlightSquare">
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
    <div class="square light"></div>
    <div class="square dark"></div>
  </div>
</template>

<style scoped>
.board {
  display: grid;
  grid-gap: 0;
  grid-template-columns: repeat(8, [col] 10vw);
  grid-template-rows: repeat(8, [row] 10vw);
  width: 100%;
  justify-content: center;
  align-content: center;
  margin: 0 auto;
}

.dark {
  background-color: #00a303;
}

.light {
  background-color: aquamarine;
}
.highlighted {
  background-color: rgba(255, 0, 0, 0.766);
}

/* styles for desktop screens */
@media only screen and (min-width: 1024px) {
  .board {
    grid-template-columns: repeat(8, [col] 5vw);
    grid-template-rows: repeat(8, [row] 5vw);
    width: 50%;
  }
}
</style>
