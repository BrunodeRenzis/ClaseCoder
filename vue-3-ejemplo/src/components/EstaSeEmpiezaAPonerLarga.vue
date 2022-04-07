<script>
import { ref, computed } from "vue";
/*
Creamos una propiedad computada offerPrice que nos devuelve un texto de oferta del 50% 
(dividido entre dos), y que solo se va a recalcular cuando cambie su dependencia reactiva, 
es decir, cuando cambie el valor de la variable productPrice
*/
export default {
  props: {
    price: Number
  },
  setup(props) {
    const productPrice = ref(props.price);
    const offerPrice = computed(() => `¡Oferta!: ${productPrice.value / 2}`)
    const add = () => productPrice.value++;

    return { offerPrice, add }
  }
}
</script>
