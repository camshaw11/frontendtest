<script setup></script>

<template>
  <div class="board">
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
  background-color: #8b4513;
}

.light {
  background-color: #f0d9b5;
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
