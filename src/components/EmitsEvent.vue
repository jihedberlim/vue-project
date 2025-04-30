<template>
    <div class="component">
        <h1>Component Emits Event</h1>
        <p>{{ item }} (R${{ price.toFixed(2) }})</p>
        <button @click="toAdd">Add to cart</button>
    </div>
</template>

<script setup>
    import { defineProps, defineEmits } from 'vue';

    const props = defineProps({
        item: String,
        price: Number
    })

    const emit = defineEmits(["beenAdded"])

    function toAdd() {
        emit("beenAdded", props.price)
    }
</script>