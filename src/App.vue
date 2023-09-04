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
  <!-- header -->
  <TheHeader />
  <!-- hero section -->
  <Hero />
  <!-- main -->
  <TheMain />
  <!-- footer -->
  <TheFooter />
</template>

<style lang="scss"></style>
