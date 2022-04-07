<template>
  <div @click="add">{{ productPrice }}</div>
</template>

<script>
import { ref, watch, watchEffect } from "vue";

export default {
  props: {
    price: Number
  },
  setup(props) {
    const productPrice = ref(props.price);

    // Ejecuta inmediatamente, y cada vez que cambien sus dependencias reactivas
    watchEffect(() => console.log(`watchEffect => `, productPrice.value));

    // Ejecuta la función cuando cambia la variable reactiva productPrice.
    // La función callback puede obtener el valor actual (current) y anterior (prev).
    watch(productPrice, (current, prev) => {
      console.log(`watch => current: ${current} prev: ${prev}`);
    });

    const add = () => productPrice.value++;

    // Ejecuta la función add (suma 1) cada 3 segundos
    setInterval(add, 3000);

    return {add}
  }
}
</script>
