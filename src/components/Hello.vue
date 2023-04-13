<template>
    <div>
        <h1>Hello view</h1>
        <strong>{{ name }}</strong>

        <hr>
        <job-list />
    </div>
</template>

<script lang="ts">
import { defineComponent, reactive, toRefs } from 'vue'
import JobList from './JobList.vue'


export default defineComponent({
    setup() {
        const state = reactive({
            name: "Link",
            age: 40
        })
        state.age = 90
        console.log(state.age)

        return {...toRefs(state)}
    },
    components: {
        'job-list': JobList
    }
})
</script>
