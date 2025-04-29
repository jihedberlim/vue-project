<template>
    <div class="component">
        <h1>Data Binding Component</h1>
        <p>{{ valueText }}</p>
        <!-- <input type="text" v-bind:value="valueText"> one way Data Binding -->
        <!-- <input type="text" :value="valueText" @input="(event)=>valueText = event.target.value"> two way Data Binding -->
        <input type="text" v-model="valueText"> <!-- two way Data Binding simple -->
    </div>
</template>

<script setup>
    import {ref} from "vue"

    const valueText = ref("Vue is so cool!")
</script>