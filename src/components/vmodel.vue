<template>
    Please input name:
    <input type="text" v-model="username" />
    <div>name: {{ username }}</div>
</template>
<script setup>
    import { ref } from 'vue';
    const username = ref('Lily');
</script>