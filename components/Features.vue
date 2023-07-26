<template>
  <div class="features">
    <HeroInformation
      title="It started with a small idea"
      description="A global brand with local beginnings, our story begain in a small studio in South London in early 2014"
      link="#"
      color-title="#FFF"
      color-description="#FFF"
      color-btn="#fff"
      background="#2A254B"
    />
    <img src="/img/room.jpg" class="features-img" />
  </div>
</template>

<style lang="scss" scoped>
.features {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  column-gap: 16px;
  padding: 0 80px;
  margin: 60px 0;
  @media screen and (max-width: 767px) {
    grid-template-columns: 1fr;
    row-gap: 24px;
    padding: 0;
  }
  &-img {
    object-fit: cover;
    height: 100%;
  }
}
</style>
