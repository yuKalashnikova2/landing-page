<template>
  <div class="subscribe">
    <div class="subscribe-content">
      <h3 class="subscribe-title">Join the club and get the benefits</h3>
      <span class="subscribe-description"
        >Sign up for our newsletter and receive exclusive offers on new ranges,
        sales, pop up stores and more</span
      >

      <div class="subscribe-benefits">
        <div class="subscribe-benefits__item">
          <img src="/svg/subscribe-check.svg" />
          <span>Exclusive offers</span>
        </div>
        <div class="subscribe-benefits__item">
          <img src="/svg/subscribe-check.svg" />
          <span>Large discounts</span>
        </div>
        <div class="subscribe-benefits__item">
          <img src="/svg/subscribe-check.svg" />
          <span>Free events</span>
        </div>
      </div>
        <FormSubscribe /> 
    </div>
  </div>
</template>

<style lang="scss">
.subscribe {
  background: url('/img/subscribe.jpg');
  padding: 97px 0 86px 0;
  background-size: cover;
  color: #fff;
  &-content {
    max-width: 500px;
    margin: auto;
    text-align: center;
  }

  &-title {
    display: block;
    font-size: 32px;
    font-weight: 400;
    margin: 0 0 12px 0;
  }
  &-benefits {
    display: flex;
    justify-content: center;
    margin-top: 30px;
    & > *:not(:last-child) {
      margin-right: 36px;
    }
    &__item {
      display: flex;
      align-items: center;
      gap: 8px;
    }
  }
  &-form {
    display: flex;
    margin-top: 40px;
    width: 100%;
  }
}
</style>
