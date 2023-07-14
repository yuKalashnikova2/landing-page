<script setup></script>

<template>
  <div class="hero">
    <div class="hero-info">
      <div class="hero-info__text">
        <h2 class="hero-info__title">
          Luxury homeware for people who love timeless design quality
        </h2>
        <span class="hero-info__description"
          >Shop the new Spring 2022 collection today</span
        >
      </div>
      <div class="hero-info__link">
        <NuxtLink to="#" class="hero-info__link-btn">View collection</NuxtLink>
      </div>
    </div>
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
  &-info {
    background-color: #fff;
    max-width: 630px;
    padding: 48px 55px;
    height: 444px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    &__title {
      line-height: 1.5;
      font-weight: 400;
      margin: 0 0 20px 0;
    }
    &__link {
      background: #f9f9f9;
      width: 170px;
      display: flex;
      justify-content: center;
      &-btn {
        color: #2a254b;
        padding: 16px 32px;
      }
    }
  }
}
</style>
