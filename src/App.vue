<script setup>
import MainTitle from './components/MainTitle.vue'
import BigButton from './components/BigButton.vue'
</script>

<template>
<BigButton class = "largeButton1" buttonText = "Pixel-Art" imagePath = "https://animals.net/wp-content/uploads/2018/08/Tanuki-3-650x425.jpg" />
<BigButton class = "largeButton2" buttonText = "Projects" imagePath = "https://folklorethursday.com/wp-content/uploads/2018/09/1.-Racoon-Dog-1024x768.jpg" />
<BigButton class = "largeButton3" buttonText = "About" imagePath = "https://pbs.twimg.com/media/FPZpkGOVgAAdII-.jpg" />
<MainTitle mainTitle = "Spook" subTitle = "Video game development and pixel-art" />
</template>

<style scoped>
.largeButton1{
  position: fixed;
  bottom: 0px;
  left: 0.15%;
  filter: hue-rotate(90deg);
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
