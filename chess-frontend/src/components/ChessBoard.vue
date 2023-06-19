<script setup>
import { ref, defineEmits } from 'vue'

const emit = defineEmits(['updateClickedSquareIds'])

const clickedSquareIds = ref([])
const clickedSquare = ref(null)

// handle selection of square on the board
const selectSquare = (squareId) => {
  clickedSquare.value = squareId
  clickedSquareIds.value.push(squareId)
  emit('updateClickedSquareIds', clickedSquareIds.value)
}

// check if square is currently clicked
const isClickedSquare = (squareId) => {
  return clickedSquare.value === squareId
}

// generate id of square based on the row and col position
const getSquareId = (row, col) => {
  const letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h']
  const file = letters[col - 1]
  const rank = 9 - row
  return file + rank
}
</script>
<template>
  <div class="board">
    <div v-for="col in 8" :key="col" class="col">
      <div
        v-for="row in 8"
        :key="row"
        class="square"
        :class="{ highlighted: isClickedSquare(getSquareId(row, col)) }"
        @click="selectSquare(getSquareId(row, col))"
      ></div>
    </div>
  </div>
</template>

<style scoped>
.board {
  display: grid;
  grid-template-columns: repeat(8, [col] 10vw);
  grid-template-rows: repeat(8, [row] 10vw);
  justify-content: center;
  align-content: center;
  border: 1px solid white;
}

.square {
  height: 10vw;
}

/* target every second column and colour the odd and even squares */
.col:nth-child(even) .square:nth-child(odd) {
  background-color: var(--dark);
}
.col:nth-child(even) .square:nth-child(even) {
  background-color: var(--light);
}

/* target every other column and colour the odd and even squares */
.col:nth-child(odd) .square:nth-child(odd) {
  background-color: var(--light);
}

.col:nth-child(odd) .square:nth-child(even) {
  background-color: var(--dark);
}

.square.highlighted {
  background-color: var(--highlight) !important;
}

/* styles for desktop screens */
@media only screen and (min-width: 1024px) {
  .board {
    grid-template-columns: repeat(8, [col] 5vw);
    grid-template-rows: repeat(8, [row] 5vw);
  }

  .square {
    height: 5vw;
  }
}
</style>
