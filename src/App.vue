<template>
  <div class="">{{ user.name }}</div>
  <div class="">{{ user.age }}</div>
</template>

<script>
import { reactive } from 'vue';

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
      user
    }
  }
}
</script>

<style>

</style>