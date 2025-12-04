<template>
    <div v-text="message"></div>
    <div v-html="html"></div>
</template>
<script setup>
const message = '<span>hello vue!</span>'
const html = '<strong>hello vue!</strong>'
</script>