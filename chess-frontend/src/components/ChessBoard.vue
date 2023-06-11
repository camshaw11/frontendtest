<script setup>
  import { ref, defineEmits } from 'vue';
  
  const emit = defineEmits(['updateClickedSquareIds'])

  const clickedSquareIds = ref([]);

  const highlightSquare = (e) => {
    const clickedSquare = e.target
    // only target children
    if (clickedSquare.classList.contains('square')) {
      // toggle highlighted colour
      clickedSquare.classList.toggle('highlighted')
      // add new values to array
      clickedSquareIds.value.push(clickedSquare.id)
      // emit data to parent 
      emit('updateClickedSquareIds', clickedSquareIds.value)
    }
  }

</script>
<template>
  <div class="board" @click="highlightSquare">
    <div class="square dark" id="a8"></div>
    <div class="square light" id="b8"></div>
    <div class="square dark" id="c8"></div>
    <div class="square light" id="d8"></div>
    <div class="square dark" id="e8"></div>
    <div class="square light" id="f8"></div>
    <div class="square dark" id="g8"></div>
    <div class="square light" id="h8"></div>
    <div class="square light" id="a7"></div>
    <div class="square dark" id="b7"></div>
    <div class="square light" id="c7"></div>
    <div class="square dark" id="d7"></div>
    <div class="square light" id="e7"></div>
    <div class="square dark" id="f7"></div>
    <div class="square light" id="g7"></div>
    <div class="square dark" id="h7"></div>
    <div class="square dark" id="a6"></div>
    <div class="square light" id="b6"></div>
    <div class="square dark" id="c6"></div>
    <div class="square light" id="d6"></div>
    <div class="square dark" id="e6"></div>
    <div class="square light" id="f6"></div>
    <div class="square dark" id="g6"></div>
    <div class="square light" id="h6"></div>
    <div class="square light" id="a5"></div>
    <div class="square dark" id="b5"></div>
    <div class="square light" id="c5"></div>
    <div class="square dark" id="d5"></div>
    <div class="square light" id="e5"></div>
    <div class="square dark" id="f5"></div>
    <div class="square light" id="g5"></div>
    <div class="square dark" id="h5"></div>
    <div class="square dark" id="a4"></div>
    <div class="square light" id="b4"></div>
    <div class="square dark" id="c4"></div>
    <div class="square light" id="d4"></div>
    <div class="square dark" id="e4"></div>
    <div class="square light" id="f4"></div>
    <div class="square dark" id="g4"></div>
    <div class="square light" id="h4"></div>
    <div class="square light" id="a3"></div>
    <div class="square dark" id="b3"></div>
    <div class="square light" id="c3"></div>
    <div class="square dark" id="d3"></div>
    <div class="square light" id="e3"></div>
    <div class="square dark" id="f3"></div>
    <div class="square light" id="g3"></div>
    <div class="square dark" id="h3"></div>
    <div class="square dark" id="a2"></div>
    <div class="square light" id="b2"></div>
    <div class="square dark" id="c2"></div>
    <div class="square light" id="d2"></div>
    <div class="square dark" id="e2"></div>
    <div class="square light" id="f2"></div>
    <div class="square dark" id="g2"></div>
    <div class="square light" id="h2"></div>
    <div class="square light" id="a1"></div>
    <div class="square dark" id="b1"></div>
    <div class="square light" id="c1"></div>
    <div class="square dark" id="d1"></div>
    <div class="square light" id="e1"></div>
    <div class="square dark" id="f1"></div>
    <div class="square light" id="g1"></div>
    <div class="square dark" id="h1"></div>
  </div>
</template>

<style scoped>
.board {
  display: grid;
  grid-gap: 0;
  grid-template-columns: repeat(8, [col] 10vw);
  grid-template-rows: repeat(8, [row] 10vw);
  justify-content: center;
  align-content: center;
}

.dark {
  background-color: var(--dark);
}

.light {
  background-color: var(--light);
}
.highlighted {
  background-color: var(--highlight);
}

/* styles for desktop screens */
@media only screen and (min-width: 1024px) {
  .board {
    grid-template-columns: repeat(8, [col] 5vw);
    grid-template-rows: repeat(8, [row] 5vw);
    /* width: 50%; */
  }
}
</style>
