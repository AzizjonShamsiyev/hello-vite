<template>
    <div v-for="(item,index) in list" :key="index">
        index is : {{ index }} --- element content is : {{ item }}
    </div>
</template>
<script setup>
    import { reactive, ref } from 'vue';
    const list = reactive(['HTML', 'CSS', 'JavaScript', 'Vue']);
</script>