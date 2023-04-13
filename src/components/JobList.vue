<template>
  <div>
    <ul>
      <li v-for="job in jobs" :key="job.id">
        <h3>{{ job.title }} in {{ job.location }}</h3>
        <p class="salary">Salary: {{ job.salary }}</p>
        <p>Active: <span :class="{active: job.is_active, 'deactive': job.is_active==false  }">{{ job.is_active ? 'Active': 'Inactive'}}</span></p>
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import Job from "../types/Job";
import { defineComponent, onActivated, ref, toRefs } from "vue";

export default defineComponent({
  setup() {
    const jobs = ref<Job[]>([
      {
        id: 1,
        title: "Software Engineer",
        location: "Dhaka, Bangladesh",
        salary: 500000,
        is_active: true,
        active_class: 'active'
      },
      {
        id: 2,
        title: "Frontend Engineer",
        location: "CT, Bangladesh",
        salary: 40000,
        is_active: false,
        active_class: 'deactive'
      },
      {
        id: 3,
        title: "Architech Engineer",
        location: "Noakhali, Bangladesh",
        salary: 80000,
        is_active: true,
        active_class: 'active'
      },
      {
        id: 4,
        title: "CIVIL Engineer",
        location: "Khulna, Bangladesh",
        salary: 300000,
        is_active: true,
        active_class: 'active'
      },
      {
        id: 5,
        title: "API Engineer",
        location: "Dhaka, Bangladesh",
        salary: 344444,
        is_active: false,
        active_class: 'deactive'
      },
      {
        id: 6,
        title: "Project Manager",
        location: "Noakhali, Bangladesh",
        salary: 500000,
        is_active: true,
        active_class: 'active'
      },
      {
        id: 7,
        title: "Auto Engineer",
        location: "Dhaka, Bangladesh",
        salary: 500000,
        is_active: false,
        active_class: 'deactive'
      },
      {
        id: 8,
        title: "Machanical Engineer",
        location: "Dhaka, Bangladesh",
        salary: 500000,
        is_active: true,
        active_class: 'active'
      },
      {
        id: 9,
        title: "Hardware Engineer",
        location: "Dhaka, Bangladesh",
        salary: 500000,
        is_active: false,
        active_class: 'deactive'
      },
    ]);

    return { jobs };
  },
});
</script>

<style scoped>
ul {
  list-style: none;
}
ul li {
  background: #221d1d;
  margin: 15px 0px;
  padding: 15px 10px;
  color: #fff;
}
.active {
    color: white;
    background: green;
    padding: 4px 25px;
    border-radius: 15px;
}
.deactive {
    color: white;
    background: #b30808;
    padding: 4px 25px;
    border-radius: 15px;
}
</style>
