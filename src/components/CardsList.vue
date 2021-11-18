<template>
  <div class="catalog">
    <card />
  </div>
</template>

<script>
import Card from "./Card.vue";
export default {
  name: "AllContent",

  components: {
    Card,
  },
};
</script>.

<style lang="scss" scoped>
  .catalog {
    width: 66vw;
    height: 141vh;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr 1fr 1fr;
    grid-column-gap: 3vw;
    grid-row-gap: 3vh;
  }

  @media screen and (max-width: 1200px ) {
    .catalog {
      width: 100%;
      height: 237vh;
      grid-template-columns: 1fr 1fr ;
      grid-template-rows: repeat(5 1fr);
      grid-row-gap: 4.2vh;
      grid-column-gap: 3vw;
    }
  }

  @media screen and (max-width: 480px ) {
    .catalog {
      width: 100%;
      height: 429vh;
      grid-template-columns: 1fr ;
      grid-template-rows: repeat(9 1fr);
      margin-top: 2vh;
    }
  }
</style>