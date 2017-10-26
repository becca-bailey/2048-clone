<template>
  <div :class="[`board__tile--${color}`]">
    {{ number }}
  </div>
</template>

<script>
  const combos = [
    { number: 2, color: 'yellow' },
    { number: 4, color: 'blue' },
    { number: 8, color: 'orange' },
  ];

  function getRandomInt(min, max) {
    const min1 = Math.ceil(min);
    const max1 = Math.floor(max);
    return Math.floor(Math.random() * (max1 - min1)) + min1;
  }

  function getRandomNumber() {
    return combos[getRandomInt(0, 3)];
  }

  export default {
    data() {
      const n = getRandomNumber();
      return {
        number: n.number,
        color: n.color,
      };
    },
  };

</script>

<style scoped>
  [class^="board__tile"] {
    align-items: center;
    background-color: lightgray;
    display: flex;
    height: 90%;
    justify-content: center;
    position: relative;
    width: 90%;
    font-size: 3em;
  }

  .board__tile--blue {
    background-color: darkcyan;
  }

  .board__tile--orange {
    background-color: darkorange;
  }

  .board__tile--yellow {
    background-color: yellow;
  }

</style>
