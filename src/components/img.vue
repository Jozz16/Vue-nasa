<template>
  <div class="hello">
    <div class="container">
      <img :src="img" class="img-fluid">
    </div>
  </div>



</template>

<script>
export default {
  name: 'ImgNasa',
  props: {
    img: String
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container { 
  max-width: 100%;
  max-height: 100%;
}
.img-fluid {
  width: 1000px;
  height: 600px;
  
}
</style>
