<script setup>
import ChessBoard from './components/ChessBoard.vue'

import { ref } from 'vue'

const clickedSquareIds = ref([])

const handleClickedSquareIdsUpdate = (data) => {
  clickedSquareIds.value = data
}
</script>

<template>
  <header>
    <h1 class="title">chessboard.</h1>
  </header>
  <main>
    <div class="container">
      <ChessBoard @updateClickedSquareIds="handleClickedSquareIdsUpdate" />
      <aside class="sidebar">
        <ol>
          <li v-for="id in clickedSquareIds" :key="id">{{ id }}</li>
        </ol>
      </aside>
    </div>
  </main>
</template>

<style scoped>
.title {
  margin-bottom: 0.5em;
}

.container {
  width: 100%;
  height: 100%;
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
}

.sidebar {
  border: 2px solid #155263;
  padding: 1em;
  margin-top: 1em;
  margin-right: 0.4em;
  margin-left: 0.4em;
  height: 8em;
  width: 100%;
  display: flex;
  background-color: white;
  overflow-y: auto;
}

/* styles for desktop screens */
@media only screen and (min-width: 1024px) {
  .container {
    flex-flow: nowrap;
    justify-content: center;
  }
  .sidebar {
    height: auto;
    max-height: 584px;
    width: 20%;
    margin-top: 0;
  }
}
</style>
