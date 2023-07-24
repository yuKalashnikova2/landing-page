<script setup>
const aboutBrandItems = ref([
  {
    title: 'Next day as standard',
    text: 'Order before 3pm and get your order the next day as standard',
    link: '/svg/about-brand-delivery.svg',
  },
  {
    title: 'Made by true artisans',
    text: 'Handmade crafted goods made with real passion and craftmanship',
    link: '/svg/about-brand-check.svg',
  },
  {
    title: 'Unbeatable prices',
    text: 'For our materials and quality you won’t find better prices anywhere',
    link: '/svg/about-brand-purchase.svg',
  },
  {
    title: 'Recycled packaging',
    text: 'We use 100% recycled to ensure our footprint is more manageable',
    link: '/svg/about-brand-sprout.svg',
  },
])
</script>
<template>
  <div class="about-brand">
    <h2 class="about-brand__title">What makes our brand different</h2>
    <div class="about-brand-items">
      <div
        class="about-brand-item"
        v-for="(item, index) in aboutBrandItems"
        :key="index"
      >
        <div>
          <img :src="item.link" class="about-brand-item__img"/>
          <h3 class="about-brand-item__title">{{ item.title }}</h3>
          <span class="about-brand-item__description">{{ item.text }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.about-brand {
  padding: 80px 80px 130px 80px;
  &__title {
    text-align: center;
    color: var(--black);
    font-size: 24px;
    margin: 0 0 36px 0;
  }
  &-items {
    display: flex;
    justify-content: space-around;
    color:var(--black);
    & > *:not(:last-child) {
      margin-right: 18px;
    }
  }
  &-item {
    padding: 48px;
    background-color: #f9f9f9;
    &__img {
        display: block;
        margin-bottom: 12px;
    }
    &__title {
        margin: 0 0 12px 0;
        font-size: 20px;
    }
    &__description {
        font-size: 16px;
        line-height: 1.5;
    }
  }
}
</style>
