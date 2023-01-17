<template>
  <!-- data binding digunakan untuk membuat data dinamis -->
  <!-- notasinya: v-bind dapat dipersingkat juga dengan: -->
  <a :href="url">Go To Gihub Nenti</a>
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      url:'https://github.com/nentinur'
    }   
  },
  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
