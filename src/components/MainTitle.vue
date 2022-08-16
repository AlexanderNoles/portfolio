<script setup>
defineProps({
  mainTitle: String,
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
        <div class = "sourceLink">
          <a href="https://github.com/AlexanderNoles/portfolio" > [Source Code] </a>
          <a href="https://mobile.twitter.com/ramen_is_fine" > [Twitter] </a>
        </div>
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
  border-bottom: 4px solid rgb(0, 0, 0);
  filter: drop-shadow(0 -6px 0.75rem black);

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
.sourceLink{
  position: absolute;
  left: 75%;
  right: 5%;
  bottom: 20%;
  top: 20%;
  font-size: 15px;
  display: inline-block;
  color: red;
}
</style>
