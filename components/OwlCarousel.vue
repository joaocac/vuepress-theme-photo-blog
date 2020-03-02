<template>
    <div class="hero-slides">
        <VueOwlCarousel :autoplay="true">
            <div v-for="(entry, idx) in heroEntries" v-bind:key="idx" class="single-hero-slide bg-img slide-background-overlay" :style="getStyle(entry)">
                <div class="container h-100">
                    <div class="row h-100 align-items-end">
                        <div class="col-12">
                            <div class="hero-slides-content">
                                <div class="line"></div>
                                <h2>{{entry.title}}</h2>
                                <p>{{entry.description}}</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </VueOwlCarousel>
    </div>
</template>

<script>
// import Carousel from 'VueOwlCarousel'

export default {
    components: {
        VueOwlCarousel,
    },

    props: ['heroEntries'],

    methods: {
      getStyle(item) {
        return `background-image: url(${item.image})`
      }
    }
}
</script>
