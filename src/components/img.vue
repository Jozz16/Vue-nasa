<template>
  <div class="hello">
    <div class="container">
      <img :src="nasaImg" class="img-fluid">
    </div>
  </div>



</template>

<script>
import axios from 'axios'
export default {
  name: 'ImgNasa',
  props: {
    msg: String
  },
  data () {
    return {
      nasaImg: null
    }
  },
  mounted () {

    const x_api_key = 'DLLiELxaRGmu2QNUiD26kzW9clIivHoFXGgQLuRX'
    axios({
      method: 'get',
      url: `https://api.nasa.gov/planetary/apod?api_key=${x_api_key}`
    }).then(resp => {
      console.log(resp)
      this.nasaImg = resp.data.url
    })
  }
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
