<template>
<div id="wrapper">
    <div class="swiper-container">
        <div class="swiper-wrapper">
            <slide-one></slide-one>
            <slide-two></slide-two>
            <slide-three></slide-three>
            <slide-four></slide-four>
            <slide-five></slide-five>
            <slide-six></slide-six>
            <slide-seven></slide-seven>
            <slide-eight></slide-eight>
        </div>
    </div>
    <div class="pagination-wrapper">
        <div class="swiper-pagination"></div>
    </div>
</div>
</template>

<script>
import Swiper from 'swiper';
import SlideOneVue from './slides/SlideOne';
import SlideTwoVue from './slides/SlideTwo.vue';
import SlideThreeVue from './slides/SlideThree.vue';
import SlideFourVue from './slides/SlideFour.vue';
import SlideFiveVue from './slides/SlideFive.vue';
import SlideSixVue from './slides/SlideSix.vue';
import SlideSevenVue from './slides/SlideSeven.vue';
import SlideEightVue from './slides/SlideEight.vue';

export default {
  data() {
    return {
        mySwiper,
    }
  },
  props: {
    
  },
  components: {
    slideOne: SlideOneVue,
    slideTwo: SlideTwoVue,
    slideThree: SlideThreeVue,
    slideFour: SlideFourVue,
    slideFive: SlideFiveVue,
    slideSix: SlideSixVue,
    slideSeven: SlideSevenVue,
    slideEight: SlideEightVue
  },
  mounted() {
    this.mySwiper = new Swiper('.swiper-container', {
      loop: true,
      autoplay: {
        delay: 3000,
      },
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
        clickable: true,
        renderBullet: function (index, className) {
          return `<span style="width: 20px; height: 20px; margin: 0px 10px;" class="` + className + `">` + (index + 1) + `</span>`;
        }
      }
    //   simulateTouch: false,
    //   allowTouchMove: false
    });
  }
}
</script>

<style>
    @import '../../node_modules/swiper/dist/css/swiper.min.css';

    html, body {
      height: 100%;
    }

    #wrapper {
        background-color: transparent;
        width: 100%;
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
      margin: 5% auto 0 auto;
    }

    .swiper-wrapper {
      width: 100%;
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
      width: 20px !important;
      height: 20px !important;
      text-align: center;
      line-height: 20px;
      font-size: 12px;
      color:#000;
      opacity: 1;
      background: rgba(0,0,0,0.2);
    }
    .swiper-pagination-bullet-active {
      color:#fff;
      background: #007aff;
    }

    .logoWrapper {
      text-align: center;
      height: 100%;
    }

</style>
