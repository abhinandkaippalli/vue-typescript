<template>
  <div class="app">
    <JobList :jobs="jobs" />
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import JobList from './components/JobList.vue'
import Job from './types/job';

export default defineComponent({
  name: 'App',
  components: {
    JobList
  },
  setup() {
  //   const name = ref('Abhi')
  //   const age = ref<number | string>(25)

  //  const changeName = (newName: string) => {
  //     name.value = newName
  //     return name.value
  //   }

  //   const changeAge = (newAge: number | string) => {
  //     age.value = newAge
  //     return age.value
  //   }
  //   return {
  //   name,
  //   age,
  //   changeName,
  //   changeAge
  // }

  const jobs = ref<Job[]>([
    { title: 'farm worker', location: 'lon lon ranch', salary: 30000, id: '1' },
      { title: 'quarryman', location: 'death mountain', salary: 40000, id: '2' },
      { title: 'flute player', location: 'the lost woods', salary: 35000, id: '3' },
      { title: 'fisherman', location: 'lake hylia', salary: 21000, id: '4' },
      { title: 'prison guard', location: 'gerudo valley', salary: 32000, id: '5' }
  ])

  return { jobs }

  }
});
</script>

<style>

</style>
