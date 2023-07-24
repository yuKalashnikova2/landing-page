<script setup>
const props = defineProps({
  title: {
    type: String,
    required: false,
  },
  description: {
    type: String,
    required: false,
  },
  link: {
    type: String,
    required: false,
  },
  colorTitle: {
    type: String,
    default: '',
  },
  colorDescription: {
    type: String,
    default: '#5B5676',
  },
  colorBtn: {
    type: String,
    default: '#2a254b',
  },
  background: {
    type: String,
    default: '#fff',
  },
})
</script>
<template>
  <div class="hero-info" :style="{ backgroundColor: background }">
    <div class="hero-info__text">
      <h2 class="hero-info__title" :style="{ color: colorTitle }">
        {{ title }}
      </h2>
      <span
        class="hero-info__description"
        :style="{ color: colorDescription }"
        >{{ description }}</span
      >
    </div>
    <div class="hero-info__link">
      <NuxtLink
        :to="link"
        class="hero-info__link-btn"
        :style="{ color: colorBtn }"
        >View collection</NuxtLink
      >
    </div>
  </div>
</template>

<style lang="scss">
.hero {
  &-info {
    background-color: #fff;
    max-width: 630px;
    padding: 48px 55px;
    min-height: 444px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    &__title {
      line-height: 1.5;
      font-weight: 400;
      margin: 0 0 20px 0;
    }
    &__link {
      background: rgba(249, 249, 249, 0.15);
      width: 170px;
      display: flex;
      justify-content: center;
      &:hover {
        background: rgba(249, 249, 249, 0.4);
      }
      &-btn {
        padding: 16px 32px;
      }
    }
  }
}
</style>
