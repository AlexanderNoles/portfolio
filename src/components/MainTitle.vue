<script setup>
defineProps({
  mainTitle: {
    type: String,
    required: true
  },
  subTitle: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class = "base"> 
    <div class = "mainTitle">
      {{ mainTitle }}
      <div class = "subTitle">
        {{ subTitle }}
      </div>
    </div> 
  </div>

</template>
<style scoped>
.base{
  position: fixed;
  padding: 5px;
  padding-top: 0px;
  top: 0;
  left: 0;
  width: 100%;
  background: #242424;

  -webkit-user-select: none; /* Safari */        
  -moz-user-select: none; /* Firefox */
  -ms-user-select: none; /* IE10+/Edge */
  user-select: none; /* Standard */
}
.mainTitle {
  font-size: 35px;
  text-align: center;
}
.subTitle {
  font-size: 20px;
}
</style>
