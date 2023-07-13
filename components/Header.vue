<script setup>
const menu = [
  { name: 'Plant pots', path: '/plant' },
  { name: 'Ceramics', path: '/plant' },
  { name: 'Tables', path: '/plant' },
  { name: 'Chairs', path: '/plant' },
  { name: 'Crockery', path: '/plant' },
  { name: 'Tableware', path: '/plant' },
  { name: 'Cutlery', path: '/plant' },
]
</script>
<template>
  <header class="header">
    <div class="header-top">
      <div class="header-top-search">
        <img src="/svg/header-search.svg" />
      </div>
      <div class="header-logo">
        <NuxtLink to="#">Avion</NuxtLink>
      </div>
      <div class="header-top-right">
        <div class="header-top-right__cart">
          <NuxtLink to="#">
            <img src="/svg/header-cart.svg" />
          </NuxtLink>
        </div>
        <div class="header-top-right__user">
          <NuxtLink to="#">
            <img src="/svg/header-user.svg" />
          </NuxtLink>
        </div>
      </div>
    </div>

    <div class="header-menu">
      <NuxtLink
        class="header-menu__link"
        :to="item.path"
        v-for="(item, index) in menu"
        :key="index"
      >
        {{ item.name }}
      </NuxtLink>
    </div>
  </header>
</template>

<style lang="scss" scoped>
.header {
  height: 132px;
  background: #fff;
  &-top {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    height: 70px;
    border-bottom: 1px solid rgba(0, 0, 0, 0.1);
    margin: 0 28px;
    align-items: center;
    &-right {
      display: flex;
      align-items: center;
      justify-content: flex-end;
      &__cart {
        margin-right: 16px;
      }
    }
  }
  &-logo {
    font-family: 'Kenarose', sans-serif;
    font-size: 24px;
    text-decoration: none;
    text-align: center;
    &:hover {
      text-decoration: underline;
    }
  }
  &-menu {
    height: 62px;
    display: flex;
    justify-content: center;
    align-items: center;
    & > *:not(:last-child) {
      margin-right: 44px;
    }

    &__link {
      color: #726e8d;
      &:hover {
        text-decoration: underline;
      }
    }
  }
}
</style>
