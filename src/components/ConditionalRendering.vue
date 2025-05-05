<template>
    <div class="component">
        <h1>Conditional Rendering Component</h1>
        <p>Name: {{ namePerson }}</p>
        <p v-if="numDogs === 0">There are no dogs</p>
        <p v-else-if="numDogs === 1">There's a dog</p>
        <p v-else>There are many dogs</p>
    </div>
</template>

<script setup>
    import { defineProps } from 'vue';

    defineProps({
        namePerson: String,
        numDogs: Number
    })
</script>