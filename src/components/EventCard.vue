<template>
    <div class="event-card">
        <h2>{{ event.title }}</h2>
        <span>{{ event.date }}</span>
        <span style="padding-left:10px">{{ event.time }}</span>
        <hr>
        <article>
            {{ event.description }}
        </article>
    </div>
</template>

<script lang="ts" setup>

import Event from '@/types/Event'

defineProps<{
    event: {
    type: Event,
    required: true
    }
}>()

// import { ref } from "vue";

// const event = ref({
//   id: 1,
//   category: "Shufflester",
//   title: "Bos taurus",
//   description: "Quisque erat eros, viverra eget, congue eget, semper rutrum, nulla. Nunc purus. Phasellus in felis. Donec semper sapien a libero. Nam dui. Proin leo odio, porttitor id, consequat in, consequat ut, nulla. Sed accumsan felis. Ut at dolor quis odio consequat varius. Integer ac leo. Pellentesque ultrices mattis odio.",
//   location: "787 Truax Crossing",
//   time: "1:41 AM",
//   date: "4/20/2022",
//   petsAllowed: true,
//   organizer: "Cow, scottish highland"
// })


</script>

<style scoped>
    .event-card {
        background: #cdcacadd;
        color: #111;
        padding: 15px 10px; 
        margin-bottom: 12px;
        cursor: pointer;
    }
</style>
