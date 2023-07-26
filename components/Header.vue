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

const isOpenedMobileMenu = ref(false)
</script>
<template>
  <header class="header">
    <div class="header-top">
      <div class="header-top-left">
        <div class="header-top-search">
          <img src="/svg/header-search.svg" />
        </div>
        <div
          class="header-top-mobile-menu"
          @click="isOpenedMobileMenu = !isOpenedMobileMenu"
        >
          <img src="/svg/mobile-menu.svg" />
        </div>
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
    <div class="heder-menu-mobile" v-if="isOpenedMobileMenu">
      <NuxtLink
        class="header-menu-mobile-link"
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
  @media screen and (max-width: 767px) {
    position: relative;
    height: auto;
  }
  &-top {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    height: 70px;
    border-bottom: 1px solid rgba(0, 0, 0, 0.1);
    margin: 0 28px;
    align-items: center;
    @media screen and (max-width: 767px) {
      margin: 0;
      border-bottom: none;
      height: 0;
      padding: 20px 0 20px 24px;
      display: flex;
      justify-content: space-between;
    }
    &-mobile-menu {
      display: none;
      @media screen and (max-width: 767px) {
        display: block;
      }
    }
    &-left {
      display: flex;
      gap: 20px;
      @media screen and (max-width: 767px) {
        order: 2;
      }
    }
    &-right {
      display: flex;
      align-items: center;
      justify-content: flex-end;
      @media screen and (max-width: 767px) {
        display: none;
      }
      &__cart {
        margin-right: 16px;
      }
    }
  }
  &-logo {
    font-family: 'Kenarose', sans-serif;
    color: var(--black-second);
    font-size: 24px;
    text-decoration: none;
    text-align: center;
    &:hover {
      text-decoration: underline;
    }
    @media screen and (max-width: 767px) {
      order: 1;
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
    @media screen and (max-width: 767px) {
      display: none;
    }

    &__link {
      color: var(--gray);
      &:hover {
        text-decoration: underline;
      }
    }
    &-mobile {
      position: absolute;
      background: #fff;
      top: 60px;
      width: 100%;
      padding: 40px 24px;
      &-link {
        display: block;
        margin-top: 20px;
        color: var(--gray);
        border-bottom: 1px solid rgba(85, 74, 91, 0.2);
        &:hover {
          background: rgba(85, 74, 91, 0.2);
        }
      }
    }
  }
}
</style>
