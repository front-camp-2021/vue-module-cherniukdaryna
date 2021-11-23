<template>
  <div class="catalog">
    <card v-for="item in resultList" :key="item.id" :productsList="item"/>
  </div>
</template>

<script>
import Card from "./Card.vue";

export default {
  name: "AllContent",

  components: {
    Card,
  },

  props: {
    currentPage: {
      type: Number,
      requier: false,
    },
    categories: {
      type: Array,
      requier: false,
    },
    brands: {
      type: Array,
      requier: false,
    },
    input: {
      type: String,
      requier: false,
    }
  },

  data() {
    return {
      cardsList: [],
    }
  },

  beforeMount(){
    this.getProducts();
  },
  methods: {
    async getProducts(){
      const res = await fetch('http://localhost:3001/products');
      const data = await res.json();
      this.cardsList = data;
    }
  },

  computed: {
    resultList(){
      return this.cardsList
      .filter((item) => item.title.toLowerCase().includes(this.input, 0))
      .filter((item) => this.categories.length > 0 ? this.categories.includes(item.category) : item.category)
      .filter((item) => this.brands.length > 0 ? this.brands.includes(item.brand) : item.brand)
      .slice(this.currentPage * 9 - 9, this.currentPage * 9);
    }
  },
  
};
</script>

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