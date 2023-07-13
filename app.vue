<template>
  <div class="flex">
    <div class="container">
      <Header />
      <div class="content-wrapper">
        <NuxtPage />
      </div>
    </div>
  </div>
</template>

<style lang="scss">
@import url('https://fonts.cdnfonts.com/css/satoshi');
@import url('https://fonts.cdnfonts.com/css/kenarose');
* {
  box-sizing: border-box;
}

body {
  font-family: 'Satoshi', sans-serif;
  min-height: 100vh;
}

a {
  text-decoration: none;
  color: #22202e;
}

ul li {
  list-style-type: none;
}
.container {
  margin: 0 auto;
  max-width: 1440px;
  background: rgb(197, 230, 234);
}
</style>
