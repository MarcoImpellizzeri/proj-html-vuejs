<script >
import TheHeader from './components/TheHeader.vue';
import Hero from './components/Hero.vue';
import TheMain from './components/TheMain.vue';
import TheFooter from './components/TheFooter.vue';

export default {
  components: {
    TheHeader,
    Hero,
    TheMain,
    TheFooter
  }
}
</script>

<template>
  <a href="#0" class="square top">
    <i class="fa-solid fa-folder"></i>
    <p>Prebuilds</p>
  </a>
  <a href="#0" class="square bot">
    <i class="fa-solid fa-cart-shopping"></i>
    <p>Buy Now</p>
  </a>

  <!-- header -->
  <TheHeader />
  <!-- hero section -->
  <Hero />
  <!-- main -->
  <TheMain />
  <!-- footer -->
  <TheFooter />
</template>

<style lang="scss">
@use "../src/style/partials/variables" as *;


.square {
  border-radius: 10px;
  position: fixed;
  width: 66px;
  background-color: $my-white-color;
  z-index: 9999;
  aspect-ratio: 1/1;
  box-shadow: rgba(2, 2, 2, 0.15) 0px 3px 15px 0px;
  font-size: .8rem;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  text-decoration: none;
  color: #33475B;

  i {
    font-size: 1.3rem;
    margin: 5px;
  }

  p {
    margin: 0;
    font-size: .7rem;
  }
}

.top {
  top: 160px;
  right: 15px;
}

.bot {
  top: 235px;
  right: 15px;
}
</style>
