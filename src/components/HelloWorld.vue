<template>
  <div>
    <h1>Hello Wrold</h1>
    {{ name }}

    <hr>
    <button type="button" @click="nameChange('Sakib Khan')">Change name</button>
    <hr>
    <h3>Age : {{ age }}</h3>
    <button @click="chnageAge('40')">Chnage Age</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  data() {
    return {
      name: "Sahadat",
      age: 20 as number | string
    }  
  },
  methods: {
    nameChange(name: string )  {
      this.name = name
    },
    chnageAge(age: number | string) {
      this.age = age
    }
  }
})
</script>
