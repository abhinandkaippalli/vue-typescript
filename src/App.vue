<template>
  <div class="app">
   <p>Hello, {{ name }} - {{ age }}</p>
   <button @click="changeName('Abhinand')">Change name</button>
   <button @click="changeAge('30')">change age</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'App',
  components: {},
  data : function() {
    return {
      name : 'Abhi',
      age: 25 as number | string
    }
  },
  methods: {
    changeName(name:string) {
      this.name = name
      return name
    },
    changeAge(age: number | string) {
      this.age = age
      return age
    }
  }
});
</script>

<style>

</style>
