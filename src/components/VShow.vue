<template>
    <p v-if="flag">v-if</p>
    <p v-show="flag">v-show</p>
    <button @click="flag = !flag">Click</button>
</template>
<script setup>
    import { ref } from 'vue';
    const flag = ref(true);
</script>