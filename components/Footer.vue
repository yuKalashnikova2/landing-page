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

        <div class="footer-subscribe">
          <span>Join our mailing list</span>
          <FormSubscribe
            different-color="light"
            bg-color-input="rgba(255,255,255,0.15)"
            bgColorInputText="#fff"
          />
        </div>
      </div>

      <div class="footer-copyright">
        <span class="footer-copyright__name">Copyright 2023 Avion LTD</span>
        <div class="footer-copyright__social">
          <NuxtLink to="#">
            <img src="../public/svg/social/lnk.svg" />
          </NuxtLink>
          <NuxtLink to="#">
            <img src="../public/svg/social/facebook.svg" />
          </NuxtLink>
          <NuxtLink to="#">
            <img src="../public/svg/social/inst.svg" />
          </NuxtLink>
          <NuxtLink to="#">
            <img src="../public/svg/social/skype.svg" />
          </NuxtLink>
          <NuxtLink to="#">
            <img src="../public/svg/social/pint.svg" />
          </NuxtLink>
        </div>
      </div>
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
    border-bottom: 1px solid var(--violet);
  }
  &-menu {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    padding-bottom: 48px;
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
  &-copyright {
    display: flex;
    justify-content: space-between;
    padding-top: 24px;
    &__name {
      font-size: 14px;
    }
    &__social {
      display: flex;
      & > *:not(:last-child) {
        margin-right: 24px;
      }
    }
  }
}
</style>
