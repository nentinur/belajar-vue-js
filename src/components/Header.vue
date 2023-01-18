<!-- component baru -->
<template>
    <!-- menampilkan props -->
    <h2>PROPS: {{ text }}</h2>
</template>

<script>
export default {
    name: "Header",
    // menangkap props dari App.vue
    props:["text"],
}
</script>

<style>
</style>
