<script>
export default{
  emits: ['activated'],
  methods:{
    CloseInParent(e){
      this.$emit('activated')
    }
  }
}
</script>

<template>
<img class="main" @click="CloseInParent" src="https://cdn-icons.flaticon.com/png/512/2961/premium/2961937.png?token=exp=1660685613~hmac=ac116fa6e37df07692563cc18687c66d"/>
</template>

<style scoped>
.main{
  width: 30px;
  height: 30px;
  position: fixed;
  top: 5px;
  right: 5px;
}
</style>
