<!-- 
    Aufgabe 1: Momentan ist der Inhalt h1 statisch(Ich bin statisch).
    Sorge dafür, dass der Inhalt in einer Variable definiert werden kann und dynamisch ist.
-->

<script setup>

let title = "Ich bin dynamisch";
</script>


<template>
    <div class="title">
        <h1>{{ title }}</h1>
    </div>
</template>

<style>
.title {
    display: flex;
    justify-content: center;
}
</style>