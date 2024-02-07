<template>
  <div id="app">
    <SwiperGallery :products="productsData" />
  </div>
</template>

<script>
import SwiperGallery from './components/SwiperGallery.vue';

export default {
  components: {
    SwiperGallery,
  },
  data() {
    return {
      productsData: [
        {
          id: 1,
          imageUrl: require('./assets/ds-t1-mq.png'),
          alt: 'Ben & Ante'
        },
        {
          id: 2,
          imageUrl: require('./assets/ds-t2-mq.png'),
          alt: 'Ante & Ben'
        }
      ],
    };
  },
};
</script>
