<template>
  <div class=" bg-white text-gray-600 leading-normal text-base tracking-normal">
      <NavComponent/>
      <BannerComponent/>
      <StoreComponent/>
      <AboutComponent/>
      <FooterComponent/>
  </div>
</template>

<script setup>
import AboutComponent from './components/AboutComponent.vue'
import BannerComponent from './components/BannerComponent.vue'
import FooterComponent from './components/FooterComponent.vue'
import NavComponent from './components/NavComponent.vue'
import StoreComponent from './components/StoreComponent.vue'
</script>
