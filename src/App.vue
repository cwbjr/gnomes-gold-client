<template>
  <div id="app">
    <router-view :image="imageList"/>
  </div>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      imgURL: '../../static/img_url.json',
      imageList: {}
    }
  },
  mounted () {
    this.getImageData()
  },
  methods: {
    getImageData () {
      fetch(this.imgURL)
        .then(res => res.json())
        .then((data) => {
          this.imageList = data.imgLoc[0]
          console.log(this.imageList.iphone)
        })
    }
  }
}
</script>

<style>
html {
  height: 100%;
  overflow: hidden;
}

body {
  background-image:linear-gradient(rgba(0, 0, 255, 0.1), rgba(255, 255, 0, 0.1)), url("../static/img/body-pic-1.jpg/");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  margin:0 auto;
  padding:0;
  perspective: 1px;
  transform-style: preserve-3d;
  height: 100%;
  overflow-y: scroll;
  overflow-x: hidden;
}
</style>
