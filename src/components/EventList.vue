<template>
  <div class="event-list" style="margin-top: 20px">
    <h1>Event List</h1>
    <event-card v-for="event in events" :key="event.id" :event="event" />
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import EventCard from "@/components/EventCard.vue";
import Event from "@/types/Event";

export default defineComponent({
  setup() {
    const events = ref<Event[]>([
      {
        id: 1,
        category: "Shufflester",
        title: "Bos taurus",
        description:
          "Quisque erat eros, viverra eget, congue eget, semper rutrum, nulla. Nunc purus. Phasellus in felis. Donec semper sapien a libero. Nam dui. Proin leo odio, porttitor id, consequat in, consequat ut, nulla. Sed accumsan felis. Ut at dolor quis odio consequat varius. Integer ac leo. Pellentesque ultrices mattis odio.",
        location: "787 Truax Crossing",
        time: "1:41 AM",
        date: "4/20/2022",
        petsAllowed: true,
        organizer: "Cow, scottish highland",
      },
      {
        id: 2,
        category: "Twiyo",
        title: "Junonia genoveua",
        description:
          "Vivamus metus arcu, adipiscing molestie, hendrerit at, vulputate vitae, nisl. Aenean lectus. Pellentesque eget nunc. Donec quis orci eget orci vehicula condimentum. Curabitur in libero ut massa volutpat convallis. Morbi odio odio, elementum eu, interdum eu, tincidunt in, leo. Maecenas pulvinar lobortis est. Phasellus sit amet erat. Nulla tempus.",
        location: "7183 Hauk Hill",
        time: "3:18 PM",
        date: "6/6/2022",
        petsAllowed: false,
        organizer: "Genoveva",
      },
      {
        id: 3,
        category: "Riffwire",
        title: "Ursus maritimus",
        description:
          "Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Mauris viverra diam vitae quam. Suspendisse potenti. Nullam porttitor lacus at turpis. Donec posuere metus vitae ipsum. Aliquam non mauris. Morbi non lectus. Aliquam sit amet diam in magna bibendum imperdiet. Nullam orci pede, venenatis non, sodales sed, tincidunt eu, felis. Fusce posuere felis sed lacus.",
        location: "026 Summer Ridge Pass",
        time: "6:08 PM",
        date: "1/12/2023",
        petsAllowed: false,
        organizer: "Polar bear",
      },
      {
        id: 4,
        category: "Kimia",
        title: "Philetairus socius",
        description:
          "Pellentesque viverra pede ac diam. Cras pellentesque volutpat dui. Maecenas tristique, est et tempus semper, est quam pharetra magna, ac consequat metus sapien ut nunc. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Mauris viverra diam vitae quam. Suspendisse potenti. Nullam porttitor lacus at turpis.",
        location: "2 Melby Junction",
        time: "8:46 PM",
        date: "12/7/2022",
        petsAllowed: false,
        organizer: "Weaver, sociable",
      },
      {
        id: 5,
        category: "Realfire",
        title: "Vulpes chama",
        description:
          "Praesent blandit lacinia erat. Vestibulum sed magna at nunc commodo placerat. Praesent blandit. Nam nulla. Integer pede justo, lacinia eget, tincidunt eget, tempus vel, pede.",
        location: "27 American Ash Pass",
        time: "12:29 AM",
        date: "12/16/2022",
        petsAllowed: false,
        organizer: "Fox, silver-backed",
      },
      {
        id: 6,
        category: "Voonix",
        title: "Panthera leo persica",
        description:
          "Integer ac neque. Duis bibendum. Morbi non quam nec dui luctus rutrum. Nulla tellus.",
        location: "7890 Troy Circle",
        time: "10:47 PM",
        date: "9/20/2022",
        petsAllowed: false,
        organizer: "Asian lion",
      },
      {
        id: 7,
        category: "Ainyx",
        title: "Drymarchon corias couperi",
        description:
          "Donec quis orci eget orci vehicula condimentum. Curabitur in libero ut massa volutpat convallis. Morbi odio odio, elementum eu, interdum eu, tincidunt in, leo. Maecenas pulvinar lobortis est. Phasellus sit amet erat. Nulla tempus.",
        location: "443 Fulton Center",
        time: "3:49 PM",
        date: "8/23/2022",
        petsAllowed: true,
        organizer: "Eastern indigo snake",
      },
      {
        id: 8,
        category: "Gigaclub",
        title: "Bubo virginianus",
        description:
          "Duis bibendum, felis sed interdum venenatis, turpis enim blandit mi, in porttitor pede justo eu massa. Donec dapibus. Duis at velit eu est congue elementum.",
        location: "81 Cherokee Parkway",
        time: "11:51 PM",
        date: "10/21/2022",
        petsAllowed: true,
        organizer: "Owl, great horned",
      },
      {
        id: 9,
        category: "Rhyzio",
        title: "Geochelone radiata",
        description:
          "Pellentesque viverra pede ac diam. Cras pellentesque volutpat dui. Maecenas tristique, est et tempus semper, est quam pharetra magna, ac consequat metus sapien ut nunc. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Mauris viverra diam vitae quam. Suspendisse potenti. Nullam porttitor lacus at turpis. Donec posuere metus vitae ipsum.",
        location: "43754 East Way",
        time: "4:06 PM",
        date: "2/1/2023",
        petsAllowed: false,
        organizer: "Radiated tortoise",
      },
      {
        id: 10,
        category: "Wordpedia",
        title: "Turtur chalcospilos",
        description:
          "Sed accumsan felis. Ut at dolor quis odio consequat varius. Integer ac leo.",
        location: "73 Ruskin Place",
        time: "1:01 PM",
        date: "4/25/2022",
        petsAllowed: false,
        organizer: "Emerald-spotted wood dove",
      },
    ]);

    return {events};
  },
  components: {
    "event-card": EventCard,
  },
});
</script>
