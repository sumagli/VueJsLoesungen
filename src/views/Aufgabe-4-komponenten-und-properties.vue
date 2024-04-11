<!-- 
    Aufgabe 4: Lagere die Buttons in eine Komponente aus und rufe diese 3 mal auf.
-->
<script setup>
import LinkingButton from "../components/Aufgabe-4/LinkingButton.vue";
const redirect = (url) => {
    window.open(url, '_blank').focus();
}
</script>

<template>
    <div class="container">
        <LinkingButton name="Youtube" link="https://youtube.com" />
        <LinkingButton name="X(Ehemals Twitter)" link="https://x.com" />
        <LinkingButton name="Instagram" link="https://Instagram.com" />
    </div>
</template>

<style scoped>
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