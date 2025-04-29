<template>
    <div class="component">
        <h1>Data Components</h1>
        <p>Name: {{ nameProduct }} - {{ codProduct }}</p>
    </div>
</template>

<script setup>
    const nameProduct = "Book"
    const codProduct = "#987"
</script>

<!-- <script>
    //options API - antigamente utilizada no Vue2
    // export default {
    //     data: function() {
    //         return {
    //             nameProduct: "Pencil",
    //             codProduct: "#321"
    //         }
    //     }
    // }

    // composition API - utilizado a partir do Vue3
    // export default {
    //     setup:function() {
    //         const nameProduct = "Pen"
    //         const codProduct = "#789"
    //         return {nameProduct, codProduct}
    //     }
    // }
</script> -->