<template>
  <!-- CONDITIONAL DAN LOOP -->

  <!-- IF
  If ini akan menampilkan data, jika datanya ada,
  dan menampilkan tulisan "No Data Found", jika datanya tidak ada -->
  <div v-if="product.length">
  <ul>
    <!-- FOR -->
    <li v-for="item in product" :key="item.id">
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
      
      product: [
        // { id: 1, title: "product 1", price: 30000 },
        // { id: 2, title: "product 2", price: 20000 },
        // { id: 3, title: "product 3", price: 10000 },
        // { id: 4, title: "product 4", price: 50000 },
        // { id: 5, title: "product 5", price: 40000 }
      ]
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
