<template>
  <new-component :price="{number:5}"/>
  <form-prueba v-model:name="name" v-model:age="age" v-model:color="color" />
  <vue-reactive :price="{number:10}"/>
  <reactive-vs-ref/>
  <esta-se-empieza-a-poner-larga/>
  <watch-effect/>
  <compo-suspenso/>
  <teleport-component/>
</template>

<script>
import NewComponent from './components/NewComponent.vue'
import FormPrueba from './components/FormPrueba.vue'
import VueReactive from './components/VueReactive.vue'
import ReactiveVsRef from './components/ReactiveVsRef.vue'
import EstaSeEmpiezaAPonerLarga from './components/EstaSeEmpiezaAPonerLarga.vue'
import WatchEffect from './components/WatchEffect.vue'
import CompoSuspenso from './components/CompoSuspenso.vue'
import TeleportComponent from './components/TeleportComponent.vue'

export default {
  name: 'App',
  components: {
    NewComponent,
    FormPrueba,
    VueReactive,
    ReactiveVsRef,
    WatchEffect,
    EstaSeEmpiezaAPonerLarga,
    CompoSuspenso,
    TeleportComponent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
