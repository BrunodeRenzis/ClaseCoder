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
    const productPrice = reactive({
      name: "Product Name",
      price: props.price
    });
    const add = () => productPrice.price++;

    return { productPrice, add }
  }
}
</script>
