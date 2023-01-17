<template>
  <!-- TWO WAY DATA BINDING
  Data Binding ini berlaku 2 arah, jika kita mengubah tulisan yang ada di input text, 
  maka data di variabel nama juga berubah -->
  <input type="text" v-model="nama">
  <h5>Nama: {{ nama }}</h5>
  
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      // begitu juga jika merubah data disini, maka nama di box input juga berubah
      nama:"Nenti"
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
