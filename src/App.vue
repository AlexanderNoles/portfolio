<script setup>
import MainTitle from './components/MainTitle.vue'
import BigButton from './components/BigButton.vue'
import CloseButton from './components/CloseButton.vue'
</script>

<script>
export default{
  data(){
    return{
      showPixelArtPage: false,
      showProjectsPage: false,
      showAboutPage: false,
      testString: "jasndkjbaskdbk" //Not used currently
    }
  },
  methods:{
    resetToLandingPage(e){
      this.showPixelArtPage = false
      this.showProjectsPage = false
      this.showAboutPage = false
    }
  }
}
</script>

<template>
<!-- Actual Pages -->
<div v-if="showPixelArtPage" class = "pagesBase pixelArtPage"> 
  <MainTitle subTitle = "Pixel-Art" />
  <CloseButton @activated="resetToLandingPage"/>
</div>
<div v-else-if="showProjectsPage" class = "pagesBase projectsPage"> 
  <MainTitle subTitle = "Projects" />
  <CloseButton @activated="resetToLandingPage"/>
</div>
<div v-else-if="showAboutPage" class = "pagesBase aboutPage"> 
  <MainTitle subTitle = "About" />
  <CloseButton @activated="resetToLandingPage"/>
</div>
<div v-else>
  <!-- LANDING PAGE -->
  <BigButton @buttonClicked="(msg) => showPixelArtPage = msg" class = "largeButton1" overlayText = "Pixel-Art" imagePath = "https://i.ibb.co/jznt4YG/Sprite-0002.png" />
  <BigButton @buttonClicked="(msg) => showProjectsPage = msg" class = "largeButton2" overlayText = "Projects" imagePath = "https://i.ibb.co/QFSGcYL/Cover-Image.png" />
  <BigButton @buttonClicked="(msg) => showAboutPage = msg" class = "largeButton3" overlayText = "About" imagePath = "https://avatars.githubusercontent.com/u/58830140?v=4" />
  <MainTitle mainTitle = "Spook" subTitle = "Video game development and pixel-art" />
</div>

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
@keyframes slideInFromBelow{
  0%{
    transform: translateY(100%);
  }
  100%{
    transform: translateY(0);
  }
}
@keyframes slideInFromLeft{
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(0);
  }
}
@keyframes slideInFromRight{
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(0);
  }
}
.pagesBase{
  display: block;
  width: 100%;
  height: 100%;
  background-color: rgb(91, 91, 91);
  position: fixed;
  bottom: 0%;
  right: 0%;
}
.pixelArtPage{
  /* Animation */
  animation: 1s ease-out 0s 1 slideInFromLeft;
}
.projectsPage{
  /* Animation */
  animation: 1s ease-out 0s 1 slideInFromBelow;
}
.aboutPage{
  /* Animation */
  animation: 1s ease-out 0s 1 slideInFromRight;
}
</style>
