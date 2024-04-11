<!-- 
    Aufgabe 6: Sorge dafür mithilfe von emits, 
    dass wenn man den button clickt die headline zu dem namen das buttons geändert wird.
-->
<script setup>
import { ref } from "vue";
import TextButton from "@/components/Aufgabe-8/textButton.vue";
const headline = ref("Veränder mich")

const showText = (name) => {
    headline.value = name;
}

</script>



<template>
    <div class="container">
        <h1>{{ headline }}</h1>
        <TextButton name="Chabos" @showText="showText" />
        <TextButton name="wissen" @showText="showText" />
        <TextButton name="wer" @showText="showText" />
        <TextButton name="der" @showText="showText" />
        <TextButton name="Babo" @showText="showText" />
        <TextButton name="ist" @showText="showText" />

    </div>
</template>

<style>
.button {
    margin-top: 20px;
    padding: 10px 20px;
    font-size: 16px;
    min-width: 300px;
    cursor: pointer;
}

.container {
    display: flex;
    flex-direction: column;
    align-items: center;
}
</style>