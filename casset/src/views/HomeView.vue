<script setup lang="ts">
import SmallVideo from '../components/SmallVideo.vue'
</script>

<template>
  <main class="p-2">
    <SmallVideo />
    <SmallVideo />
    <SmallVideo />
    <SmallVideo />
    <SmallVideo />
    <SmallVideo />
    <SmallVideo />
    <SmallVideo />
    <SmallVideo />
    <SmallVideo />
  </main>
</template>

<style scoped>

main{
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: center;
}

</style>