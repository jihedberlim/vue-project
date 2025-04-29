<template>
    <div class="component">
        <h1>Component Emits Event</h1>
        <p>{{ item }} (R${{ price.toFixed(2) }})</p>
        <button>Add to cart</button>
    </div>
</template>

<script setup>
    import { defineProps } from 'vue';

    defineProps({
        item: String,
        price: Number
    })
</script>