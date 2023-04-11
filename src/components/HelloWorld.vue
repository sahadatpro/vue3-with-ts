<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
  <div>
    <h2>{{  msg }}</h2>
  </div>
</template>

<style scoped>
</style>
