<template>
    <div class="component">
        <h1>Component Listen Event</h1>
        <p>Total: R$ {{ totalValue.toFixed(2) }}</p>

        <div class="list">
            <EmitsEvent item="Item1" :price="2.00" @been-added="updateTotal"/>
            <EmitsEvent item="Item2" :price="5.00" @been-added="updateTotal"/>
            <EmitsEvent item="Item3" :price="10.00" @been-added="updateTotal"/>
        </div>
    </div>
</template>

<script setup>
    import EmitsEvent from './EmitsEvent.vue';
    import { ref } from 'vue';

    const totalValue = ref(0)

    function updateTotal(p) {
        const valueUpdate = totalValue.value + p
        totalValue.value = +valueUpdate.toFixed(2)
    }
</script>

<style scoped>
    .list {
        display: flex;
        justify-content: space-between;
    }
</style>