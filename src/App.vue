<template>
  <div class="">{{ message }}</div>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    const message = ref("halo");

    setTimeout(() => {
      console.log(message);
      message.value = "composition api";
    }, 2000);

    return {
      message
    }
  }
}
</script>

<style>

</style>