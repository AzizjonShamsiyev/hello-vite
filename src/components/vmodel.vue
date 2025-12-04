<template>
    <input type="text" v-model.number="n1"> + <input type="text" v-model.number="n2"> = {{ n1 + n2 }}
</template>
<script setup>
    import { ref } from 'vue';
    const n1 = ref(0);
    const n2 = ref(0);
</script>