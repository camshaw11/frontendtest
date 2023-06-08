<script setup>
import ChessBoard from './components/ChessBoard.vue'
</script>

<template>
  <header>
    <h1>chessboard.</h1>
  </header>
  <main>
    <div class="container">
      <ChessBoard />
      <div class="sidebar">sidebar here</div>
    </div>
  </main>
</template>

<style scoped>
.container {
  border: 2px solid green;
  padding: 1em;
  width: 100%;
  display: flex;
  flex-flow: row wrap;
}
.sidebar {
  padding: 2em;
  /* border: 2px solid green; */
  min-height: 4em;
  width: 100%;
}

/* styles for desktop screens */
@media only screen and (min-width: 1024px) {
  .container {
    flex-flow: nowrap;
  }
}
</style>
