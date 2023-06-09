<script setup>
import ChessBoard from './components/ChessBoard.vue'
</script>

<template>
  <header>
    <h1 class="title">chessboard.</h1>
  </header>
  <main>
    <div class="container">
      <ChessBoard />
      <aside class="sidebar"></aside>
    </div>
  </main>
</template>

<style scoped>

.title {
  margin-bottom: 0.5em;
}
.container {
  width: 100%;
  /* padding: 1em; */
  display: flex;
  flex-flow: row wrap;
}
.sidebar {
  border: 2px solid green;
  margin-top: 1em;
  margin-right: 0.4em;
  margin-left: 0.4em;
  min-height: 8em;
  width: 100%;
  display: flex;
  background-color: white;
}

/* styles for desktop screens */
@media only screen and (min-width: 1024px) {
  .container {
    flex-flow: nowrap;
  }
}
</style>
