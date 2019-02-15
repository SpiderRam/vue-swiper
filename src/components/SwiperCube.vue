<template>
<div id="swiper-wrapper">
    <div class="swiper-container">
        <div class="swiper-wrapper">
            <div class="swiper-slide" style="background-image:url(http://lorempixel.com/600/600/nature/1)">
                <a href="https://github.com/SpiderRam" target="_blank"><div class="clickable"></div></a>
            </div>
            <div class="swiper-slide" style="background-image:url(http://lorempixel.com/600/600/nature/2)"></div>
            <div class="swiper-slide" style="background-image:url(http://lorempixel.com/600/600/nature/3)"></div>
            <div class="swiper-slide" style="background-image:url(http://lorempixel.com/600/600/nature/4)"></div>
            <div class="swiper-slide" style="background-image:url(http://lorempixel.com/600/600/nature/5)"></div>
        </div>
    </div>
    <div class="pagination-wrapper">
        <div class="swiper-pagination"></div>
    </div>
</div>
</template>

<script>
import Swiper from 'swiper';

export default {
  data() {
    return {
        mySwiper,
    }
  },
  props: {
    
  },
  mounted() {
    this.mySwiper = new Swiper('.swiper-container', {
      loop: true,
      effect: 'cube',
      grabCursor: true,
      cubeEffect: {
        shadow: true,
        slideShadows: true,
        shadowOffset: 20,
        shadowScale: 0.94,
      },
      pagination: {
        el: '.swiper-pagination',
      },
    //   simulateTouch: false,
    //   allowTouchMove: false
    });
  }
}
</script>

<style scoped>
    @import '../../node_modules/swiper/dist/css/swiper.min.css';

    html, body {
      /* position: relative; */
      height: 100%;
    }

    body {
      background: #fff;
      font-family: Helvetica Neue, Helvetica, Arial, sans-serif;
      font-size: 14px;
      color:#000;
      margin: 0;
      padding: 0;
    }

    .swiper-container {
      width: 300px;
      height: 300px;
      margin-top: 5%;
    }

    .swiper-slide {
      background-position: center;
      background-size: cover;
    }

    .clickable {
        width: 100%;
        height: 100%;
    }

    .pagination-wrapper {
        margin-top: 5%;
    }

    .swiper-pagination {
        position: relative;
    }

    .swiper-pagination-bullet {
        margin: 0px 5px !important;
    }

</style>
