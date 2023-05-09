<template>
  <div>
    <p class="nasa-title">{{ title }}</p>
  </div>
</template>

<script>
export default {
  name: "TitleNasa",
  props: {
    title: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.nasa-title {
  font-family: "Roboto Mono", monospace;
  font-size: 2rem;
  font-weight: 700;
  color: #fff;
  text-shadow: 2px 2px #000;
  background: linear-gradient(to right, #1a1a1a, #404040);
  padding: 10px 20px;
  border-radius: 5px;
}
</style>
