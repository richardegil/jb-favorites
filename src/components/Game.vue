<template>
  <div class="game drag-element">
    <p>{{ title }}</p>
    <img :src=thumbnail alt="">
  </div>
</template>

<script setup>
const props = defineProps({
  title: String,
  thumbnail: String
})
</script>

<style scoped>
/* .game {
   display: flex;
   flex-direction: column-reverse;
   flex: 0 0 18%;
   width: 100%;
   height: auto;
 }

 .game img {
   width: 100%;
   max-width: 100%;
   height: auto;
 } */
</style>