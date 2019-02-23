<template>
  <div class="swiper-slide" id="slideSeven">
    <div class="logoWrapper"> 
        <img src="../../assets/mySqlLogo.png" class="cubeImage" id="mySqlLogo">
        <br>
        <img src="../../assets/sequelizeLogo.png" class="cubeImage" id="sequelizeLogo">
    </div>
  </div>
</template>

<script>
// import JQuery from 'jquery'
// let $ = JQuery

export default {
    
};
</script>

<style scoped>
    #slideSeven {
        border: 1px solid navy;
        position: relative;
    }

    #mySqlLogo {
        float: right;
    }

    #sequelizeLogo {
        float: left;
        vertical-align: bottom;
        position: absolute;
        top: 7rem;
        right: 9rem;
    }
</style>