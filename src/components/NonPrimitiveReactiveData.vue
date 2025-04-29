<template>
    <div class="component">
        <h1>Non-Primitive Reactive Data</h1>
        <p>Name: {{ person.name }} | Age: {{ person.age }}</p>
        <button @click="changeName()">Change Name</button>
        <button @click="changeAge()">Change Age</button>
    </div>
</template>

<!-- <script setup>
    import {reactive} from "vue"

    const person = reactive({name: "Elmograbi", age: 29})

    function changeName() {
        person.name = "Berlim"
    }

    function changeAge() {
        person.age += 1
    }
</script> -->

<script>
    export default{
        data:function() {
            return {
                person: {
                    name: "Jihed",
                    age: 29
                }
            }
        },
        methods:{
            changeAge:function() {
                this.person.age +=1
            },
            changeName:function() {
                this.person.name = "Jihed Berlim"
            }
        }
    }
</script>