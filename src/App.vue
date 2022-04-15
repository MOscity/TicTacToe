<template>
<div class="container">
<span ref='confetti'></span>
  <Board @winner='fireConfetti'/>
</div>
</template>

<script>
import Board from './components/Board.vue'
import { confetti } from '../../node_modules/dom-confetti/src/main.js';

export default {
  name: 'App',
  components: {
    Board,
  },
  methods: {
    fireConfetti () {
      confetti(this.$refs.confetti)
    }
  }
}
</script>

<style scoped>
.container {
    display: grid;
    place-items: center;
    gap: 4rem;
    position: relative;
}
</style>