<script setup></script>

<template>
  <div class="hero">
    <HeroInformation
      title="Luxury homeware for people who love timeless design quality"
      description="Shop the new Spring 2023 collection today"
      link="#"
      color-link="light"
    />
    <img src="/img/hero-block.png" class="hero-image__mobile" />
  </div>
</template>

<style lang="scss">
.hero {
  background: url('/img/hero-block.png');
  height: 704px;
  background-size: cover;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  padding-right: 80px;
  &-image__mobile {
    display: none;
  }
  @media screen and (max-width: 767px) {
    display: block;
    height: auto;
    background: transparent;
    padding-right: 0px;
    &-image__mobile {
    display: block;
  }
  }
}
</style>
