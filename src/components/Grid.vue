<template>
    <div class="container-fluid">
        <div class="row">
            <app-header></app-header>
        </div>
        <div class="row">
            <app-swiper-cube></app-swiper-cube>
        </div>
        <!-- <div class="row">
            Footer            
        </div> -->
    </div>
</template>

<script>
import SwiperCubeVue from './SwiperCube.vue';
import HeaderVue from './Header.vue';
// import ScrollVue from './Scroll.vue';
// import AboutVue from './About.vue';

export default {
    components: {
        appSwiperCube: SwiperCubeVue,
        appHeader: HeaderVue,
        // appScroll: ScrollVue,
        // appAbout: AboutVue
    },
};
</script>

<style scoped>
body {
    background-image: linear-gradient(#cfe2cf, #609f60);
}
</style>
