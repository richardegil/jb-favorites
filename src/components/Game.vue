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
p {
  font-weight: 700;
 }

 .drag-element:active {
   cursor: grabbing;
   background-color: aqua;
   box-shadow: 12px 12px 24px 0px rgba(0, 0, 0, 0.08);
 }

 .drag-element:focus {
   cursor: grabbing;
 }
</style>