<script setup>
import {ref, computed} from "vue";
// ref = variable réactives
// reactive= objets reactifs
//computed = fonctions reactives
// watched= exécute en cas de changement= code réactif
// let counter = 0;
const counter =ref(0);

const printCounter = computed(()=>{
    return `xxx ${counter.value*2} xxx`
}
)

function increase(){
    counter.value++;
    console.log(counter.value);

}
function decrease(){
    counter.value--;
    console.log(counter.value);
}
</script>

<template>
    <p>
        <button @click="decrease">-</button>
        {{ counter }}
        <button @click="increase">+</button>
        <button @click.once="increase">+</button>
        {{ printCounter }}
    </p>
</template>