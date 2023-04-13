<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import Hello from './components/Hello.vue'
import EventList from '@/components/EventList.vue'


</script>

<template>
  <header>
    <div class="app">
      <HelloWorld/>
    </div>
    <hr>
    <event-list />
  </header>

  <main>
      <Hello/>
    </main>
</template>

<style scoped>
</style>
