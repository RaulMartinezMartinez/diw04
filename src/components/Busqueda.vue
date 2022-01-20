<template>
  <section id="barra-busqueda">
      <form @submit.prevent="handleEnviar">
          <input type="text" placeholder="Buscar productos ...">
          <button class="boton">Buscar</button>
      </form>
  </section>
</template>

<script>
export default {
    name: 'BarraBusqueda',
    methods: {
        handleSutmit() {
            console.log("Busqueda enviada")
        }
    }
}
</script>

<style scoped>
#barra-busqueda {
    margin: 2rem;
}
#barra-busqueda form {
    display: flex;
    justify-content: center;
    align-items: center;
}
#barra-busqueda input{
    margin: 1rem;
    padding: 0.7rem 1rem;
    border: 2px solid black;
}
.boton{
    display: flex;
    font-size: 1rem;
    background-color: white;
    border: solid black 2px;
}
.boton:hover{
    background-color: red;
}
</style>