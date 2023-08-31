<script >
import TheHeader from './components/TheHeader.vue';
import Hero from './components/Hero.vue';
import TheMain from './components/TheMain.vue';

export default {
  components: {
    TheHeader,
    Hero,
    TheMain
  }
}
</script>

<template>
  <!-- header -->
  <TheHeader />
  <Hero />
  <TheMain />
</template>

<style lang="scss"></style>
