<script>
export default
defineProps({
  buttonText: String,
  imagePath: String
})

methods: {
  onButtonClick: function(){
    console.console.log("lmao kekw");
  }
}
</script>

<template>
  <img class="base" src="../assets/images/blank.png" @click="onButtonClick" />
</template>

<style scoped>
.base{
  height: 1px;
  width: 1px;
}
</style>
