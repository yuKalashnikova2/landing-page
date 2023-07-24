<script setup>
const products = ref([
  { id: 1, img: '/img/product-1.jpg', title: 'The Dandy chair', price: 250 },
  { id: 2, img: '/img/product-2.jpg', title: 'Rustic Vase Set', price: 155 },
  { id: 3, img: '/img/product-3.jpg', title: 'The Silky Vase', price: 125 },
  { id: 4, img: '/img/product-4.jpg', title: 'The Lucy Lamp', price: 399 },
])
</script>
<template>
  <div class="products-container">
    <div class="products">
      <ProductCard
        v-for="product in products"
        :key="product.id"
        :img="product.img"
        :title="product.title"
        :price="product.price"
      />
    </div>
    <div class="products-link">
      <ButtonUI type="link" colorBtn="light" to="#">View collection</ButtonUI>
    </div>
  </div>
</template>

<style lang="scss">
.products {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  column-gap: 20px;
  margin: 0 80px 0 80px;
  &-link {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 40px;
  }
}
</style>
