
<template>

  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <TitleNasa :title= nasaTitle   />
    <ImgNasa :img= nasaUrl />
  </div>
</template>

<script>
// instalar bootstrap 
// y hechar un ojo a axios
import ImgNasa from './components/img.vue'
import TitleNasa from './components/title.vue'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    ImgNasa,
    TitleNasa
  },
   data () {
    return {
      nasaTitle: null,
      nasaUrl: null
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
      this.nasaUrl = resp.data.url
    })
  }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
   position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: #222;
}

</style>
