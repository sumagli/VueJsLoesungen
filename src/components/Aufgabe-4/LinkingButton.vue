<script setup>
const props = defineProps({
    link: {
        type: String,
        required: true
    },
    name: {
        type: String,
        required: true
    }
})
</script>

<template>
    <button class="button" @click="redirect(link)"> {{ name }}</button>
</template>

<style></style>
