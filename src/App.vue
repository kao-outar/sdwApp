<script setup>
import Test from "@/components/Test.vue";
import Counter from "@/components/Counter.vue";
import Name from "@/components/Name.vue";
import Style from "@/components/Style.vue";
import Chat from "@/components/Chat.vue";
</script>

<template>
    <Chat />
    
    <Style />
    <Counter />
    <Counter />
    <Name />
    <Name /> 
    <h1>HOLA</h1>
    <Test />
    <Test>xxxx</Test>

    <Test title="hola" />
    <Test title="hola">
        <p>Ceci est un slot</p>
    </Test>
</template>

<style scoped>

</style>
