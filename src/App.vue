<template>
  <!-- COMPUTED PROPERTIES
    properti yang dapat digunakan untuk mendefinisikan data yang nilainya tergantung dari data lain
  -->
  <input type="text" placeholder="Cari" v-model="cari">
  <ul>
    <li v-for="item in caridata" :key="item.id">
      {{ item.title }} - {{ item.price }}
    </li>
  </ul>
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      cari:"",
      products: []
    }   
  },
  created() {
    // data ini dipanggil setelah komponen dibuat di lifecycle hooks
    this.products = [
      { id: 1, title: "buku", price: 30000 },
      { id: 2, title: "penggaris", price: 20000 },
      { id: 3, title: "pensil", price: 10000 },
      { id: 4, title: "spidol", price: 50000 },
      { id: 5, title: "penghapus", price: 40000 }
    ]
  },

  //Computed propeeties
  computed: {
    // disini kita akan membuat fungsi untuk mencari data product berdasakan titlenya
    caridata() {
      // menggunakan fungsi dari JavaScript yaitu filter() dan match()
      return this.products.filter((item) => {
        return item.title.match(this.cari)
      })
    }
  }
}
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
