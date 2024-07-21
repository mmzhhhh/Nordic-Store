<template>
  <div class="max-w-[1600px] mx-auto">
    <swiper 
    :slides-per-view="1" 
    :loop="true" 
    :autoplay="{ delay: 3000, disableOnInteraction: false }"
    :modules="[Autoplay, Navigation]" 
    navigation>
      <swiper-slide v-for="(image, index) in images" :key="index" :style="{'background-image':`url(${image.src})`,'height':'64vh', 'background-size': 'cover',
        'background-position': 'center'}">
        <h1 class=" text-black text-3xl my-5 tracking-wide">{{ image.title }}</h1>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Navigation, Autoplay } from 'swiper/modules';
import 'swiper/swiper-bundle.css';
import { ref } from 'vue';

const images = ref([
  {
    title: "Stripy Zig Zag Jigsaw Pillow and Duvet Set",
    src: 'https://images.unsplash.com/photo-1422190441165-ec2956dc9ecc?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1600&q=80',
  },
  {
    title: "Real Bamboo Wall Clock",
    src: 'https://images.unsplash.com/photo-1533090161767-e6ffed986c88?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjM0MTM2fQ&auto=format&fit=crop&w=1600&q=80',
  },
  {
    title: "Brown and blue hardbound book",
    src: 'https://images.unsplash.com/photo-1519327232521-1ea2c736d34d?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1600&q=80'
  }
]);



</script>

<style scoped>
.swiper {
  width: 100%;
  height: 100%;
  background: #000;
}

.swiper-slide {
  font-size: 18px;
  color: #fff;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
  padding: 40px 60px;
}

.parallax-bg {
  position: absolute;
  left: 0;
  top: 0;
  width: 130%;
  height: 100%;
  -webkit-background-size: cover;
  background-size: cover;
  background-position: center;
}

.swiper-slide .title {
  font-size: 41px;
  font-weight: 300;
}

.swiper-slide .subtitle {
  font-size: 21px;
}

.swiper-slide .text {
  font-size: 14px;
  max-width: 400px;
  line-height: 1.3;
}

  </style>