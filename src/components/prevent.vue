<template>
  <div v-on:click="show('I am a father element even')">
    <button v-on:click="show('I am a son element event')">
      event bubbling
    </button>
    <button v-on:click.stop="show('I am a son element event')">
      prevent event bubbling
    </button>
  </div>
</template>
<script setup>
let show = (message) => console.log(message);
</script>
