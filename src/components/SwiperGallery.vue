<template>
    <div class="col-span-5 lg:col-span-2 lg:col-start-2 col-start-1 flex items-center justify-center h-full bg-black">
      <Swiper ref="swiperRef" class="w-full bg-black">
        <SwiperSlide v-for="product in products" :key="product.id" class="flex items-center justify-center bg-black">
          <img
            :src="product.imageUrl"
            :alt="product.alt"
            class="mx-auto rounded-2xl"
            style="max-width: 100%; max-height: 100vh;"
          />
        </SwiperSlide>
      </Swiper>
    </div>
  </template>
  
  <script>
  import { Swiper, SwiperSlide } from 'swiper/vue';
  
  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    props: {
      products: {
        type: Array,
        required: true,
      },
    },
  };
  </script>
