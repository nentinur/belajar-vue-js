<template>
  <!-- LIFECYCLE HOOKS
  LifeCycle Hooks adalah jendela dimana Library yang digunakan bekerja dibalik layar
  LifeCycle hooks memungkinakan untuk mengetahui komponen yang dibuat ditambahkan ke DOM, diperbarui, atau dihancurkan -->
  <div v-if="products.length">
  <ul>
    <li v-for="item in products" :key="item.id">
      {{ item.title }} - {{ item.price }}
    </li>
  </ul>
  </div>
  <div v-else>
    <p>
      No Data Found
    </p>
  </div>
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      products: []
    }   
  },
  // LifeCycle Hooks
  // urutan dijalankannya adalah beforeCreate - created - beforeMount - mount,
  // meskipun tataletaknya diacak, urutannya akan tetap seperti itu
  beforeCreate() {
    // jika ingin menjalankan fungsi, yang ingin dieksekusi sebelum komponen dibuat, maka kita harus meletakkannya di beforeCreate
    console.log('Before Create')
  },
  created() {
    // jika ingin membuat perintah setelah komponen dibuat, maka kita meletakkannya di created
    console.log('Created')

    // data ini dipanggil setelah komponen dibuat di lifecycle hooks
    this.products = [
      { id: 1, title: "product 1", price: 30000 },
      { id: 2, title: "product 2", price: 20000 },
      { id: 3, title: "product 3", price: 10000 },
      { id: 4, title: "product 4", price: 50000 },
      { id: 5, title: "product 5", price: 40000 }
    ]
  },
  beforeMount() {
    // jika ingin menjalankan fungsi setelah created, kita harus meletakkannya di beforeMount
    console.log('Before Mount')
  },
  mounted() {
    // jika ingin menjalankan fungsi setetah komponen mounted ke DOM, maka kita harus meletakkannya di mounted
    console.log('Mounted')
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
