<template>
  <h2>{{ halo }}</h2>
  <button @click="changeName">{{bahasa}}</button>
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      halo: 'Halo, Selamat datang di Website Nenti',
      bahasa: 'Turn To English'
    }   
  },
  methods: {
    changeName() {
      this.halo = "Hi, Welcome to Nenti's website",
      this.bahasa = 'Bahasa Indonesia'
    }
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
  margin-top: 60px;
}
</style>
