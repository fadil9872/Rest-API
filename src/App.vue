<template>
  <div class="">{{ name }}</div>
  <div class="">{{ age }}</div>
</template>

<script>
import { reactive, toRefs } from 'vue';

export default {
  setup() {
    const user = reactive({
      name: "M Fadil",
      age: "19"
    });

    setTimeout(() => {
      user.name = "Mukhamad Fadil";
    }, 2000);

    return {
      ...toRefs(user),
    }
  }
}
</script>

<style>

</style>