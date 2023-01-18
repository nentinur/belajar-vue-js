<!-- component baru -->
<template>
    <!-- menampilkan props -->
    <h2>PROPS: {{ text }}</h2>
    <button @click="changeText">Ubah Text</button>
</template>

<script>
export default {
    name: "Header",
    // menangkap props dari App.vue
    props: ["text"],
    data() {
        return {
            newText:"ini text dari header.vue"
        }
    },
    methods: {
        changeText() {
            this.$emit("changeTitle", this.newText)
        }
    },
    // untuk menghilangkan error warning karena $emit
    emits: ["changeTitle"],
}
</script>

<style>
</style>
