<template>
  <div >
  <p class="nasa-title">{{nasaTitle}}</p>
  </div>



</template>

<script>
import axios from 'axios'
export default {
  name: 'TitleNasa',
  props: {
    msg: String
  },
  data () {
    return {
      nasaTitle: null
    }
  },
  mounted () {

    const x_api_key = 'DLLiELxaRGmu2QNUiD26kzW9clIivHoFXGgQLuRX'
    axios({
      method: 'get',
      url: `https://api.nasa.gov/planetary/apod?api_key=${x_api_key}`
    }).then(resp => {
      console.log(resp)
      this.nasaTitle = resp.data.title
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.nasa-title {
  font-family: 'Roboto Mono', monospace;
  font-size: 2rem;
  font-weight: 700;
  color: #fff;
  text-shadow: 2px 2px #000;
  background: linear-gradient(to right, #1a1a1a, #404040);
  padding: 10px 20px;
  border-radius: 5px;
}
</style>
