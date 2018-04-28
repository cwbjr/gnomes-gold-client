<template>
  <div class="home">
    <div id="title" class="slide header">
      <h1>Gnome's Gold</h1>
    </div>
    <div id="slide1" class="slide">
      <div class="title">
        <h1>Slide 1</h1>
        <p>Lorem ipsum dolor sit amet, in velit iudico mandamus sit, persius dolorum in per, postulant mnesarchum cu nam.
          Malis movet ornatus id vim, feugait detracto est ea, eam eruditi conceptam in. Ne sit explicari interesset. Labores
          perpetua cum at. Id viris docendi denique vim.</p>
      </div>
    </div>
    <div id="slide2" class="slide">
      <div class="title2">
        <h1>Slide 2</h1>
        <p>Lorem ipsum dolor sit amet, in velit iudico mandamus sit, persius dolorum in per, postulant mnesarchum cu nam.
          Malis movet ornatus id vim, feugait detracto est ea, eam eruditi conceptam in. Ne sit explicari interesset. Labores
          perpetua cum at. Id viris docendi denique vim.</p>
      </div>
      <img :src="'../../static/img/trap.png/'">
      <img :src="'../../static/img/pot-gold-well.png/'">
    </div>
    <div id="slide3" class="slide">
      <div class="title3">
        <h1>Slide 3</h1>
        <p>Lorem ipsum dolor sit amet, in velit iudico mandamus sit, persius dolorum in per, postulant mnesarchum cu nam.
          Malis movet ornatus id vim, feugait detracto est ea, eam eruditi conceptam in. Ne sit explicari interesset. Labores
          perpetua cum at. Id viris docendi denique vim.</p>
      </div>
        <div class="phone">
        <img :src="'../../static/img/iphone3.png/'" class="back-img">
        <div>
          <iframe src="https://player.vimeo.com/video/266728295" style="position:absolute;top:0;left:0;width:40%;height:100%;"
            frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
        </div>
      </div>
      <!-- <img :src="'../../static/img/iphone3.png/'" class="back-img"> -->
    </div>
    <div id="slide4" class="slide header">
      <h1>The End</h1>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  mounted: {}
}
</script>

<style scoped>
  iframe {
    margin-left: 29%;
    margin-top: 14.4%;
    /* width: 200px;
    height: 150px; */
    z-index: 2;
  }
  /* @import url(https://fonts.googleapis.com/css?family=Nunito); */
  h1 {
    font-size: 250%;
  }

  p {
    font-size: 140%;
    line-height: 150%;
    color: #333;
  }

  .slide {
    position: relative;
    padding: 25vh 10%;
    min-height: 100vh;
    width: 100vw;
    box-sizing: border-box;
    box-shadow: 0 -1px 10px rgba(0, 0, 0, 0.7);
    transform-style: inherit;
  }

  img {
    position: absolute;
    top: 50%;
    left: 35%;
    width: 320px;
    height: 270px;
    transform: translateZ(0.35px) scale(0.75) translateX(-68%) translateY(-110%) rotate(5deg);
    padding: 10px;
    border-radius: 5px;
    background: rgba(240, 230, 220, 0.4);
    box-shadow: 0 0 8px rgba(0, 0, 0, 0.7);
  }

  img:last-of-type {
    transform: translateZ(0.5px) scale(0.6) translateX(-65%) translateY(-40%) rotate(0deg);
  }

  img.back-img {
    background: none;
    box-shadow: none;
    transform: translateZ(0.35px) scale(0.75) translateX(-50%) translateY(-15%) rotate(0deg);
    width: 75%;
    height: auto;
    top: 50%;
    left: 40%;
  }

  .slide:before {
    content: "";
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    box-shadow: 0 0 8px 1px rgba(0, 0, 0, 0.7);
  }

  .title {
    /* width: 50%; */
    margin-top: 10%;
    padding: 5%;
    border-radius: 5px;
    background: rgba(240, 230, 220, 0.7);
    box-shadow: 0 0 8px rgba(0, 0, 0, 0.7);
  }

  .title3 {
    /* width: 50%; */
    margin-top: -9%;
    padding: 5%;
    border-radius: 5px;
    background: rgba(240, 230, 220, 0.7);
    box-shadow: 0 0 8px rgba(0, 0, 0, 0.7);
  }

  .title2 {
    width: 50%;
    padding: 5%;
    border-radius: 5px;
    background: rgba(240, 230, 220, 0.7);
    box-shadow: 0 0 8px rgba(0, 0, 0, 0.7);
  }

  .slide:nth-child(2n) .title {
    margin-left: 0;
    margin-right: auto;
  }

  .slide:nth-child(2n + 1) .title2 {
    margin-left: auto;
    margin-right: 0;
  }

  .slide,
  .slide:before {
    background: 50% 50% / cover;
  }

  .header {
    text-align: center;
    font-size: 175%;
    color: #fff;
    text-shadow: 0 2px 2px #000;
  }

  #title {
    background-image: url("../../static/img/landscape.jpg/");
    z-index: 2;
  }

  #title h1 {
    transform: translateZ(0.25px) scale(0.75);
    transform-origin: 50% 100%;
  }

  #slide1 {
    background-image: url("../../static/img/well.png/");
    transform: translateZ(-1px) scale(2);
  }

  #slide2 {
    background-image: url("../../static/img/well-wall-1.jpg/");
    z-index: 2;
    /* margin-top: 4vh; */
  }

  #slide3 {
    /* background-image: url("../../static/img/iphone3.png/"); */
    transform: translateZ(-1px) scale(2);
  }

  #slide4 {
    /* background: #222; */
    background-image: url("../../static/img/ground.png/"), url("../../static/img/ground.png/"), url("../../static/img/well-rock.png/");
    background-position: center bottom, center top, center top;
    background-repeat:no-repeat, no-repeat, no-repeat;
    /* background-size: cover; */
  }

@media (max-width: 740px) {
  /* #slide2 {
    display:grid;
  } */

  img, .phone {
    display:none;
  }

  .title2 {
    width: 100%;
  }

  #slide4 {
    padding-bottom: 375px;
  }
}
</style>
