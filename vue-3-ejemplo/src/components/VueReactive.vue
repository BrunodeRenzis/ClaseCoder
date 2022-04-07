<template>
  <div @click="add">{{ productPrice }}</div>
</template>

<script>
import { reactive } from "vue";

export default {
  props: {
    price: Object
  },
  setup(props) {
    const productPrice = reactive(props.price);
    const add = () => productPrice.value++;

    return { productPrice, add }
  }
}
</script>
