<template>
  <cabecera></cabecera>
  <busqueda></busqueda>
  <camino></camino>
  <principal></principal>
  <pie></pie>
</template>

<script>
import Cabecera from './components/Cabecera.vue'
import Busqueda from './components/Busqueda.vue'
import Camino from './components/Camino.vue'
import Principal from './components/Principal.vue'
import Pie from './components/footer.vue'


export default {
  name: 'App',
  components: {
    Cabecera,
    Busqueda,
    Camino,
    Principal,
    Pie
  }
}
</script>

<style>
  html{
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    background-color: rgb(7, 134, 134);
  }
</style>
