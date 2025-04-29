<template>
    <div class="component">
        <h1>Component Listen Event</h1>
        <p>Total: R$ {{ totalValue }}</p>

        <div class="list">
            <EmitsEvent item="Item1" :price="1.99"/>
            <EmitsEvent item="Item2" :price="5.00"/>
            <EmitsEvent item="Item3" :price="10.99"/>
        </div>
    </div>
</template>

<script setup>
    import EmitsEvent from './EmitsEvent.vue';
</script>

<style scoped>
    .list {
        display: flex;
        justify-content: space-between;
    }
</style>