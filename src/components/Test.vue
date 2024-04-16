<script setup>
const pseudo="kobeni";
const names = ["Richard", "kaoutar", "mahalia"];
const prof= {
    name: "Rihcnou",
    age: 35,
};
import chat from "/img/kitten1.jpg";
let chatWidth=100;

const props=defineProps({
    title:{
    type: String,
    default:"Bonjour",
},
    color:String,
})
const toto= `<strong>Bonjour !</strong>`
</script>

<template>

    <div>{{ toto }}</div>
    <div v-text="toto" />
    <div v-html="toto" />
    <img :src="chat" :alt="chat" :width="chatWidth">
    <div :style="{backgroundColor:color}">
        <slot />    
    </div>

    <h2>{{title}} {{ pseudo }}</h2>
    {{ names[0] }}
    <ul v-if="prof.age>18">
        <li v-for="name in names">{{ name }}</li>
    </ul>
    <div v-else-if="prof.age>15"></div>
    <div v-else>Trop jeune</div>
</template>