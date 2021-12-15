<template>
  <div class="">Count : {{ counter }}</div>
  <button @click="add">Add</button>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    const counter = ref(0);

    //method 
    const add = () => {
      counter.value++;
    }
    
    return {
      counter,
      add
    }
  }
}
</script>

<style>

</style>