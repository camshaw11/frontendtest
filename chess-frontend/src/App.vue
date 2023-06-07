
<script setup>
import ChessBoard from './components/ChessBoard.vue';
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
  border: 2px solid red;
  width: 100%;
  display: flex;
  flex-flow: row wrap;
}
.sidebar {
  border: 2px solid green;
  min-height: 4em;
}
</style>
