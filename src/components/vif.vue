<template>
    <p v-if="type ==='A'">Excellent</p>
    <p v-else-if="type ==='B'">Good</p>
    <p v-else>Difference</p>
    <button @click="type='A'">Switch to Excellent</button>
    <button @click="type='B'">Switch to Good</button>
    <button @click="type='C'">Switch to Difference</button>   
</template>
<script setup>
    import { ref } from 'vue';
    const type = ref('B');
</script>