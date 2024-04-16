<!-- src/components/Exo1.vue -->
<script setup>
import { ref, computed } from "vue";
const color = ref("#FFF0F0");

const imageUrl = computed(() => {
     switch (color.value) {
        case "#FF0000":  return "/img/red.png";
        case "#00FF00":  return "/img/green.png";
        case "#0000FF":  return "/img/blue.png";
        default : return "/img/hamster.png";
     }
});
</script>
<template>
    <div :style="{ backgroundColor: color }">
        <p>
            <input v-model="color" />
            <button @click="color = '#FF0000'">R</button>
            <button @click="color = '#00FF00'">G</button>
            <button @click="color = '#0000FF'">B</button>
        </p>
        <img :src="imageUrl" alt="" />

        <img v-if="color == '#FF0000'" src="/img/red.png" alt="" />
        <img v-else-if="color == '#00FF00'" src="/img/green.png" alt="" />
        <img v-else-if="color == '#0000FF'" src="/img/blue.png" alt="" />
        <img v-else src="/img/hamster.png" alt="" />
    </div>
</template>

<style scoped>
div {
    padding: 20px;
}
img {
    width: 40%;
}
button {
    margin-left: 20px;
}
button,
input {
    font-size: 1.5em;
}
</style>
