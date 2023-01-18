<template>
  <!-- PROPS - gunakan untuk mengirimkan data dari komponen induk ke komponen anak -->
  <!-- CUSTOM EVENT - gigunakan untuk mengirimkan data dari komponen anak ke komponen induk -->
  
  <Header @changeTitle="ubahText" :text="text" />
</template>

<script>
// memanggil component Header
import Header from "@/components/Header.vue"
export default {
  name: 'App',
  // jangan lupa ditulis disini jika mau digunakan
  components: {
    Header,
  },
  data() {
    return {
      text: "ini props yang dinamis menggunakan data binding",
    };
  },
  methods: {
    ubahText(newText) {
      this.text = newText
    }
  }
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
