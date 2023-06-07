<script setup>
</script>

<template>
  <div class="board">
    board will be here
  </div>
</template>

<style scoped>
.board {
  display: grid;
  grid-gap: 0;
  grid-template-columns: repeat(8, [col] 10vw);
  grid-template-rows: repeat(8, [row] 10vw);
  width: 80vw;
  background-color: green;
  justify-content: center;
  align-content: center;
  margin: 0 auto;
}

</style>