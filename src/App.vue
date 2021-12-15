<template>
  <div class="">Count : {{ nilai }}</div>
  <button @click="add">Add</button>
</template>

<script>
import { reactive, toRefs } from 'vue';

export default {
  setup() {
    const counter = reactive({
      nilai: 0,
    });

    //method 
    const add = () => {
      counter.nilai++;
    }

    return {
      ...toRefs(counter),
      add
    }
  }
}
</script>

<style>

</style>