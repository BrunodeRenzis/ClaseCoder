<template>
  <div>{{ total }}</div>
</template>

<script>
import {onBeforeMount,onMounted} from 'vue'
export default {
  name: 'newComponent',
  props: {
      price: Number
  },
  //Con setup sepuede gestionar todo desde el mismo sin tener que detallar el tipo de propiedad, si es computada, method o lo que sea.
  //Siempre setup va a retornar lo que se necesite de cualquier componente.
  
  setup(props) {

    const total = `Total price (50% offer): ${props.price / 2}`;
    onMounted(() => console.log("mounted!"));

    /* Formato largo */

    onBeforeMount(() => {
      console.log("beforeMount hook!");
    });

    return { total }
  }
}
</script>
