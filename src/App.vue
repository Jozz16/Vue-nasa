
<template>

  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <TitleNasa />
    <ImgNasa />
  </div>
</template>

<script>
// instalar bootstrap 
// y hechar un ojo a axios
import ImgNasa from './components/img.vue'
import TitleNasa from './components/title.vue'

export default {
  name: 'App',
  components: {
    ImgNasa,
    TitleNasa
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
