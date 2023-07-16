<script setup>
const props = defineProps({
  id: {
    type: Number,
  },
  img: {
    type: String,
    required: true,
  },
  title: {
    type: String,
    required: true,
  },
  price: {
    type: Number,
    required: true,
  },
})
</script>

<template>
  <div class="product">
    <img class="product-image" :src="img" />
    <h2 class="product-title">{{ title }}</h2>
    <span class="product-price">{{ price }}£</span>
  </div>
</template>

<style lang="scss" scoped>
.product {
  &-image {
    display: block;
  }
  &-title {
    display: block;
    font-size: 20px;
    line-height: 28px;
    margin-bottom: 8px;
    cursor: pointer;
  }
  &-price {
    display: block;
    font-size: 18px;
  }
}
</style>
