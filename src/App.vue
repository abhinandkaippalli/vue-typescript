<template>
  <div class="app">
   <p>Hello, {{ name }} - {{ age }}</p>
   <button @click="changeName('Abhinand')">Change name</button>
   <button @click="changeAge('30')">change age</button>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'App',
  components: {},
  setup() {
    const name = ref('Abhi')
    const age = ref<number | string>(25)

   const changeName = (newName: string) => {
      name.value = newName
      return name.value
    }

    const changeAge = (newAge: number | string) => {
      age.value = newAge
      return age.value
    }
    return {
    name,
    age,
    changeName,
    changeAge
  }
  }
});
</script>

<style>

</style>
