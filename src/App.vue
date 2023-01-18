<template>
  <!-- menampilkan isi dari component Header -->
  <!-- mengirimkan props dari App.vue ke Header.vue -->
  <Header :text="text" />
</template>

<script>
// memanggil component Header
import Header from "@/components/Header.vue"
export default {
  name: 'App',
  // jangan lupa ditulis disini jika mau digunakan
  components: {
    Header
  },
  data() {
    return {
      text: "ini props yang dinamis menggunakan data binding",
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
</style>
