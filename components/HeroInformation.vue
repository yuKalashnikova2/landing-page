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
  colorLink: {
    type: String,
    default: false,
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
      <ButtonUI type="link" :colorBtn="colorLink || 'secondary'" to="#" mobileWidth>View collection</ButtonUI>
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
    @media screen and (max-width: 767px) {
      padding: 47px 24px 32px 24px;
      min-height: 0px;
  }
  &__text {
    margin-bottom: 32px;
  }

    &__title {
      line-height: 1.5;
      font-weight: 400;
      margin: 0 0 20px 0;
    }
  }
}
</style>
