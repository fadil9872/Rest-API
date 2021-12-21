<template>
  <div class="">Count : {{ nilai }}</div>
  <button @click="add">Add</button>

  
</template>

<script>
import { reactive, ref, watchEffect, toRefs } from 'vue';

export default {
  setup() {
    const counter = reactive({
      nilai: 0,
      foo: 'bar',
    });

    //method 
    const addNum = ref(1);

    const add = () => {
      counter.nilai++;
    }

    watchEffect(() => {
      console.log(counter.nilai);
    }, { 
      onTrigger(e) {
        console.log(e);
      },
      // onTrack(e) {
      //   console.log(e);
      // },
    }); 

    return {
      ...toRefs(counter),
      add,
    }
  }
}
</script>

<style>

</style>