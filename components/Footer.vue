<template>
  <footer class="footer">
    <div class="footer-content">
      <div class="footer-main">
        <div class="footer-menu">
          <div class="footer-menu__column">
            <span class="footer-menu__title">Menu</span>
            <NuxtLink to="/" class="footer-menu__link">New arrivals</NuxtLink>
            <NuxtLink to="/" class="footer-menu__link">Best sellers</NuxtLink>
            <NuxtLink to="/" class="footer-menu__link"
              >Recently viewed</NuxtLink
            >
            <NuxtLink to="/" class="footer-menu__link"
              >Popular this week</NuxtLink
            >
            <NuxtLink to="/" class="footer-menu__link">All products</NuxtLink>
          </div>
          <div class="footer-menu__column">
            <span class="footer-menu__title">Categories</span>
            <NuxtLink to="/" class="footer-menu__link">Crockery</NuxtLink>
            <NuxtLink to="/" class="footer-menu__link">Furniture</NuxtLink>
            <NuxtLink to="/" class="footer-menu__link">Homeware</NuxtLink>
            <NuxtLink to="/" class="footer-menu__link">Plant pots</NuxtLink>
            <NuxtLink to="/" class="footer-menu__link">Chairs</NuxtLink>
            <NuxtLink to="/" class="footer-menu__link">Crockery</NuxtLink>
          </div>

          <div class="footer-menu__column">
            <span class="footer-menu__title">Our company</span>
            <NuxtLink to="/" class="footer-menu__link">About us</NuxtLink>
            <NuxtLink to="/" class="footer-menu__link">Vacancies</NuxtLink>
            <NuxtLink to="/" class="footer-menu__link">Contact us</NuxtLink>
            <NuxtLink to="/" class="footer-menu__link">Privacy</NuxtLink>
            <NuxtLink to="/" class="footer-menu__link">Returns policy</NuxtLink>
          </div>
        </div>
      </div>
      <div class="footer-subscribe"></div>
    </div>
  </footer>
</template>

<style lang="scss">
.footer {
  background: var(--black);
  color: #fff;
  &-content {
    padding: 58px 82px 25px 82px;
  }
  &-main {
    display: grid;
    grid-template-columns: 540px 1fr;
    column-gap: 110px;
  }
  &-menu {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    &__title {
      display: block;
      margin-bottom: 12px;
    }
    &__link {
      display: block;
      color: #fff;
      font-style: 14px;
      margin-bottom: 12px;
      &:last-child {
        margin-bottom: 0;
      }
      &:hover {
        text-decoration: underline;
      }
    }
  }
}
</style>
