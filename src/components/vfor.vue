<template>
    <!-- <div v-for="(item,index) in list" :key="index">
        index is : {{ index }} --- element content is : {{ item }}
    </div> -->
    <div v-for="item in list" :key="item.id">
        id is : {{ item.id }} --- element content is : {{ item.message }}
    </div>
</template>
<script setup>
    import { reactive, ref } from 'vue';
    // const list = reactive(['HTML', 'CSS', 'JavaScript', 'Vue']);
    const list = reactive([
        { id: 1, message: 'HTML' },
        { id: 2, message: 'CSS' },
        { id: 3, message: 'JavaScript' },
        { id: 4, message: 'Vue' }
    ]);
</script>