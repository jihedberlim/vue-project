<template>
    <div class="component">
        <h1>Primitive Reactive Data</h1>
        <p>Name: {{ name }} | Age: {{ age }}</p>
        <button v-on:click="changeName()">Change Name</button>
        <button @click="changeAge()">Change Age</button>
    </div>
</template>

<script setup>
    import {ref} from "vue"
    const name = ref("Jihed")
    const age = ref(28)

    function changeName() {
        name.value = "Berlim"
    }

    function changeAge() {
        age.value += 1
    }
</script>