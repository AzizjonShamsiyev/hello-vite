<template>
    <!-- <p>username : <input type="text" v-bind:pleaceholder="username"></p> -->
    <!-- <p>password : <input type="password" :placeholder="password"></p> -->
    <button @click="showInfo">click</button>
</template>
<script setup>
const showInfo = () => {
    console.log('welcome !')
}
</script>