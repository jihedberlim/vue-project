<template>
    <div class="component">
        <h1>Assisted Properties Component</h1>
        <p>Age: {{ agePerson }}</p>
        <label>Year of Birth:</label>
        <input type="number" v-model="birthYear" min="1900">
        <label>Current Year:</label>
        <input type="number" v-model="currentYear" min="2000">
    </div>
</template>

<script setup>
    import { ref } from 'vue';
    // import { watch } from 'vue';
    import { watchEffect } from 'vue';

    const birthYear = ref(1900)
    const currentYear = ref(2000)
    const agePerson = ref(0)

    // watch(currentYear, (newYear) => {
    //     agePerson.value = newYear - birthYear.value
    // })

    // watch(birthYear, (newYear) => {
    //     agePerson.value = currentYear.value - newYear
    // })

    watchEffect(() => {
        agePerson.value = currentYear.value - birthYear.value
    })

</script>

<style scoped>
    label {
        margin: 10px;
    }
</style>