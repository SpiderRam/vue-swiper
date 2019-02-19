<template>
<div id="swiper-wrapper">
    <div class="swiper-container">
        <div class="swiper-wrapper">
            <div class="swiper-slide" id="slideOne">
              <div class="logoWrapper">
                <img src="../assets/vueLogo.png" class="cubeImage" id="vueLogo">
              </div>
            </div>
            <div class="swiper-slide" id="slideTwo">
              <div class="logoWrapper">
                <img src="../assets/polymerLogo.png" class="cubeImage" id="polymerLogo">
              </div>
            </div>
            <div class="swiper-slide" id="slideThree">
              <div class="logoWrapper">
                <img src="../assets/kendoLogo.jpg" class="cubeImage" id="polymerLogo">
                <p id="kendoText">Kendo Charts</p>
              </div>
            </div>
            <div class="swiper-slide" id="slideFour">
              <div class="logoWrapper">
                <img src="../assets/cssGridLogo.png" class="cubeImage" id="cssGridLogo">
              </div>
            </div>
            <div class="swiper-slide" id="slideFive">
              <div class="logoWrapper">
                <img src="../assets/leafletLogo.jpeg" class="cubeImage" id="leafletLogo">
              </div>
            </div>
            <div class="swiper-slide" id="slideSix">
              <div class="logoWrapper">
                <!-- <img src="../assets/leafletLogo.jpeg" class="cubeImage" id="leafletLogo"> -->

              </div>
            </div>
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
      // autoplay: {
      //   delay: 5000,
      // },
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

<style scoped>
    @import '../../node_modules/swiper/dist/css/swiper.min.css';

    html, body {
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

    #slideOne {
      border: 1px solid black;
    }

    #vueLogo {
      margin-top: 20%;
    }

    #slideTwo {
      border: 1px solid navy;
    }

    #polymerLogo {
      margin-top: 12%;
    }

    #slideThree {
      border: 1px solid green;
    }

    #kendoText {
      font-weight: bold;
      font-family: sans-serif;
    }

    #slideFour {
      border: 1px solid purple;
    }

    #cssGridLogo {
      margin-top: 40%;
    }

    #slideFive {
      border: 1px solid darkgray;
    }

    #leafletLogo {
      margin-top: 30%;
    }

    #slideSix {
      /* width: 25%; */
      background: linear-gradient(to top right, #fff calc(50% - 1px), #aaa, #fff calc(50% + 1px) )
    }

</style>
