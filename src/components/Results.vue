<template>
  <div class="results">
    <span class="results__number">7,618 results found</span>

    <button class="results__like-butn">
      <img class="results__like-image" src="@/assets/img/heart.svg" />
    </button>
  </div>
</template>

<script>
export default {
  name: "Result",
};
</script>

<style lang="scss" scoped>
.results {
  width: 100%;
  height: 4vh;
  display: flex;
  justify-content: space-between;
  flex-direction: row;
  align-items: center;
  font-size: 1.2rem;
  font-weight: 550;

  &__like-butn {
    border-radius: 8px;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.25), 0 5px 5px rgba(0, 0, 0, 0.22);
    width: 3vw;
    height: 3vw;
    background-color: #6f64f8;
    border: none;
  }

  &__like-image {
    width: 1.2vw;
    height: 1.6vh;
  }
}

@media screen and (max-width: 1200px) {
  .results__like-butn {
    width: 4vw;
  }
}

@media screen and (max-width: 720px) {
  .results {
    &__like-butn {
      width: 4vh;
      height: 100%;
    }

    &__like-image {
      width: 2vh;
      height: 2vh;
    }
  }
}

@media screen and (max-width: 480px) {
  .results {
    margin-bottom: 3vh;
  }

  .results__like-butn {
    width: 4vh;
    height: 4vh;
  }
}
</style>