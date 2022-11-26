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
img {
  padding: 0 0 1rem;
}

p {
  font-weight: 300;
}

.drag-element {
  padding: 1rem;
  border: 1px solid #ebebeb;
  border-radius: 1rem;
}

.drag-element:hover {
cursor: grab;
box-shadow: 6px 6px 12px 0px rgba(0, 0, 0, 0.08);
}

.drag-element:active {
  cursor: grabbing;
  box-shadow: 6px 6px 12px 0px rgba(0, 0, 0, 0.08);
}

.drag-element:focus {
  cursor: grabbing;
}
</style>