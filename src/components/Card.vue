<template>
  <div class="product-card">
    <div class="image">
      <img class="image__goods" src="" />
    </div>

    <div class="rating-price">
      <div class="rating">
        4,1
        <img class="rating__image-star" src="img/star.svg" />
      </div>

      <p class="price">$199</p>
    </div>

    <p class="product-card__name">JBL Speaker</p>
    <p class="product-card__information">
      Redesigned from scratch and completely revised.
    </p>

    <div class="product-card-buttons">
      <button class="product-card-buttons__wishlist">
        <img class="product-card-buttons__image-heart" src="img/heart.svg" />
        <span class="product-card-buttons__name">WISHLIST</span>
      </button>
      <button class="product-card-buttons__add">
        <img class="product-card-buttons__image-basket" src="img/basket.svg" />
        <span class="product-card-buttons__name">ADD TO CART</span>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
};
</script>

<style lang="scss" scoped>
  @import url("https://fonts.googleapis.com/css2?family=Barlow:wght@200&display=swap");
  .product-card {
    width: 20vw;
    height: 45vh;
    background-color: white;
    padding-top: 2vh;
    position: relative;
    border-radius: 8px;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.25), 0 5px 5px rgba(0, 0, 0, 0.22);

    &__name {
      margin-bottom: 0.3vh;
      margin-top: 1vh;
      font-size: 1rem;
      font-weight: 700;
    }

    &__information {
      font-size: 0.9rem;
      font-weight: 500;
    }

    &__information,
    &__name {
      margin-left: 1.3vw;
    }
  }

  .image {
    margin-bottom: 3vh;
    width: 100%;
    height: 25.2vh;
    display: flex;
    justify-content: center;
    flex-direction: row;
    align-items: center;

    &__goods {
      max-width: 90%;
      max-height: 100%;
    }
  }

  .rating-price {
    width: 100%;
    height: 2.8vh;
    line-height: 2.8vh;
    display: flex;
    justify-content: space-between;
    flex-direction: row;
    align-items: flex-start;
    font-size: 1rem;
    font-weight: 600;
  }

  .rating {
    width: 3.7vw;
    height: 100%;
    background-color: #6f64f8;
    color: white;
    text-align: center;
    border-radius: 8px;
    margin-left: 1.3vw;

    &__image-star {
      width: 1.3vh;
      height: 1.3vh;
      margin: 0 0.1vw;
    }
  }
  .price {
    margin-right: 1.3vw;
  }

  .product-card-buttons {
    position: absolute;
    bottom: 0;
    background-color: #ededed;
    width: 100%;
    height: 4.2vh;
    border-radius: 8px;

    &__image-heart,
    &__image-basket {
      width: 1.3vh;
      height: 1.3vh;
    }

    &__wishlist,
    &__add {
      width: 50%;
      height: 100%;
      font-size: 1rem;
      font-weight: 600;
      border: none;
      font-family: "Barlow", sans-serif;
    }

    &__wishlist {
      border-radius: 0 0 0 1vh;
    }

    &__add {
      border-radius: 0 0 1vh 0;
      background-color: #6f64f8;
      color: white;
    }
  }
 
  @media screen and (max-width: 1200px) {
    .product-card {
      width: 30vw;
      height: 45vh;
    }

    .rating {
      width: 7vw;
    }
  }

  @media screen and (min-width: 481px) and (max-width: 720px) {
    .product-card {
      width: 46vw;
    }
  }

  @media screen and (max-width: 480px) {
    .product-card {
      width: 100%;
      height: 45vh;
    }

    .rating {
      width: 6vh;
      height: 100%;
    }
  }
</style>
