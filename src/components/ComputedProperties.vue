<template>
    <div class="component">
        <h1>Computed Properties Component</h1>
        <p>Age: {{ agePerson }}</p>
        <label>Year of Birth:</label>
        <input type="number" v-model="birthYear" min="1900">
        <label>Current Year:</label>
        <input type="number" v-model="currentYear" min="2000">
    </div>
</template>

<script setup>
    import { ref, computed } from 'vue';

    const birthYear = ref(1900)
    const currentYear = ref(2000)
    const agePerson = computed(() => {
        return currentYear.value - birthYear.value
    })
</script>

<style scoped>
    label {
        margin: 10px;
    }
</style>