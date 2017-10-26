<template>
  <div id="board">
    <div class="board__container">
      <Tile v-for="n in 16"/>
    </div>
  </div>
</template>

<script>
  import Tile from './Tile';

  export default {
    components: {
      Tile,
    },
  };
</script>

<style scoped>
  #board {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .board__container {
    align-items: center;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-template-rows:  repeat(4, 1fr);
    justify-items: center;
    height: 500px;
    width: 500px;
  }
</style>
