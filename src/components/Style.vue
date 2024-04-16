<script setup>
import { ref } from "vue";
const isActive = ref(false);
const bgColor="#FFF6BA" ;
const fgColor="A56700" ;
</script>

<template>
    Coucou
    <div class="bg">
        <button @click="isActive =!isActive">{{ isActive }}</button>
        <p v-show="isActive"></p>

        <p :style="`background-color=${bg-color};color:red`">lorem epsum</p>
        <p :style="{backgroundColor: bgColor, color:`red`}">lorem epsum</p>

        <p :style="{backgroundColor: isActive? bgColor : ''}">lorem epsum</p>
        <p :class="{bg: isActive }">lorem epsum</p>
        <p :class="[ isActive ? 'bg': '', 'active']">lorem epsum</p>

    </div>
</template>

<style scoped>
.bg{
    background-color: aqua;
}
.active{
    border-bottom: 4px solid black;
}
</style>