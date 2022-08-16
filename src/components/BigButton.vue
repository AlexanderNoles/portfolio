<script>
export default{
  props: {
    buttonText: String,
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
  </div>
</template>

<style scoped>
.imageContainer{
  width: 33%;
  height: 100%;
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
  height: 100%;
  object-fit: cover;
}
.fullImage:hover{
  filter: blur(1.5px) contrast(200%) invert(75%);
}
.text{
  margin-top: 50%;
  text-align: center;
  font-size: 50px;
}
</style>