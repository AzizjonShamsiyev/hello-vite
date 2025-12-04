<!-- <template>{{message}}</template>
<script setup>
import { ref } from 'vue';
const message = ref('hello !')
setTimeout(() => {
    message.value = 'welcome to chine'
}, 2000)
</script> -->

<template>{{ obj.message }}</template>
<script setup>
import { reactive } from 'vue';
const obj = reactive({message: 'hi! '})
setTimeout(() =>{
    obj.message = 'vue3!'
}, 1500)
</script>