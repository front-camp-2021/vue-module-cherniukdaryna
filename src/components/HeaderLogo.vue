<template>
  <header class="header">
    <img class="header__logo-header" src="@/assets/img/logo.png" />
    <a class="header__title" href="#">Online Store</a>
  </header>
</template>

<script>
export default {
  name: "HeaderLogo",
};
</script>

<style lang="scss" scoped>

.header {
    width: 90%;
    height: 7vh;
    display: flex;
    justify-content: flex-start;
    flex-direction: row;
    align-items: center;
    margin-bottom: 3.3vh;
    padding-left: 1vw;

    &__logo-header {
        max-height: 6.67vh;
        max-width: 4.6vw;
        margin-right: 1vw;
    }

    &__title:link {
        color: 7E72F2;
        font-size: 2rem;
        font-weight: 600;
        text-decoration: none;
    }

    &__title:hover {
        text-decoration: underline;
    }
}

@media screen and (max-width: 720px) {
  .header {
    justify-content: center;
  }
}

@media screen and (max-width: 320px) {
  .header__logo-header {
    max-height: 12vh;
    max-width: 12vw;
  }
}

</style>