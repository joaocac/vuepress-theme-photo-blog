<template>
    <!-- ***** Hero Area Start ***** -->
    <section class="hero-area">
      <OwlCarousel :heroEntries="heroEntries" />
    </section>
    <!-- ***** Hero Area End ***** -->
</template>

<script>
import OwlCarousel from './OwlCarousel.vue'
export default {
    components: {
      OwlCarousel,
    },

    data() {
      return {
        heroEntries: [
          {
            image: 'img/bg-img/slide1.jpg',
            title: 'Sand Storm',
            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent vel tortor facilisis, volutpat nulla placerat, tincidunt mi. Nullam vel orci dui. Suspendisse sit amet laoreet neque. Fusce sagittis suscipit sem.',
          },
          {
            image: 'img/bg-img/slide2.jpg',
            title: 'New York',
            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent vel tortor facilisis, volutpat nulla placerat, tincidunt mi. Nullam vel orci dui. Suspendisse sit amet laoreet neque. Fusce sagittis suscipit sem.',
          },
          {
            image: 'img/bg-img/slide3.jpg',
            title: 'The Desert',
            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent vel tortor facilisis, volutpat nulla placerat, tincidunt mi. Nullam vel orci dui. Suspendisse sit amet laoreet neque. Fusce sagittis suscipit sem.',
          },
          {
            image: 'img/bg-img/slide3.jpg',
            title: 'Mountains Hike',
            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent vel tortor facilisis, volutpat nulla placerat, tincidunt mi. Nullam vel orci dui. Suspendisse sit amet laoreet neque. Fusce sagittis suscipit sem.',
          },
        ],
      }
    },

    methods: {
      getStyle(item) {
        return `background-image: url(${item.image})`
      }
    }
}
</script>
