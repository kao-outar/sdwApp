<script setup>
import {ref} from "vue";

const name = ref("KAO")
</script>
<template>
    <h1>{{ name }}</h1>
    <input type="text" v-model="name"/>

    <button @click="name+='*'">Test Name</button>
</template>