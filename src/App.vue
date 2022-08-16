<script setup>
import MainTitle from './components/MainTitle.vue'
import BigButton from './components/BigButton.vue'
</script>

<template>
<BigButton class = "largeButton1" overlayText = "Pixel-Art" imagePath = "https://i.ibb.co/jznt4YG/Sprite-0002.png" />
<BigButton class = "largeButton2" overlayText = "Projects" imagePath = "https://i.ibb.co/QFSGcYL/Cover-Image.png" />
<BigButton class = "largeButton3" overlayText = "About" imagePath = "" />
<MainTitle mainTitle = "Spook" subTitle = "Video game development and pixel-art" />
</template>

<style scoped>
.largeButton1{
  position: fixed;
  bottom: 0px;
  left: 0.15%;
}
.largeButton2{
  position: fixed;
  bottom: 0px;
  left: 33.45%;
}
.largeButton3{
  position: fixed;
  bottom: 0px;
  left: 66.75%;
}
</style>
