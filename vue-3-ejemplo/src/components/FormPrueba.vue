<template>
  <form action="">
      <input type="text" value="name">
      <input type="text" value="color">
      <input type="number" value="age">
  </form>
</template>

<script>
import {reactive} from 'vue'
export default {
    setup() {
    const name = reactive("John Doe");
    const age = reactive(33);
    const color = reactive("#FF0000");
    return {
        name, age, color
    }
    }

}
</script>

<style>

</style>