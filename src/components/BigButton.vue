<script>
export default{
  props: {
    overlayText: String,
    imagePath: String,
  },

  data(){
    return{
      testString : "@/assets/images/CoverImage.png" // not currently used
    }    
  },

  methods: {
    onButtonClick(e) {
      
    }
  }
}
</script>

<template>
  <div class = "imageContainer">
    <button class = "actualButton"> <img class = "fullImage" :src="imagePath" alt="buttonimage"/> </button>
    <div class = "text">
      <h2> {{overlayText}} </h2>
    </div>
  </div>
</template>

<style scoped>
.imageContainer{
  width: 33%;
  height: 100%;
}
.text{
  position:absolute; 
  top: 10%;
  left: 9.325%;
  right: 9.325%;
  margin-top: 50%;
  text-align: center;
  font-size: 50px;
  color: rgba(255, 255, 255, 0.9);

  width: 77.5%;

  filter: drop-shadow(0 0 0.75rem black);

  overflow: hidden;

  -webkit-user-select: none; /* Safari */        
  -moz-user-select: none; /* Firefox */
  -ms-user-select: none; /* IE10+/Edge */
  user-select: none; /* Standard */

  pointer-events: none;
}
.actualButton{
  width: 100%;
  height: 100%;
  background-color: transparent;
  background-repeat: no-repeat;
  border: none;
  cursor: pointer;
  overflow: hidden;
  outline: none;
}
.fullImage{
  width: 100%;
  height: 105%;
  outline-style: solid;
  outline-width: 0px;
  outline-color: white;
  object-fit: cover;
  transition: transform 0.3s ease;
}
.fullImage:hover{
  transform: scale(0.99);
  outline-width: 3px;
}
</style>