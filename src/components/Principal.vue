<template>
  <div id="foto">
    <img v-bind:src="bicis[0]" id="foto_principal" alt="Specialized S-Work" />
    <div id="descripcion">
      <p>
        Diseñamos la nueva Tarmac para ofrecerte una experiencia única, la
        combinación perfecta entre aerodinámica, ligereza y comodidad.
      </p>
      <p>
        Mejorando las formas de los tubos usando nuestro FreeFoil Shape Library,
        y evolucionando nuestro concepto Rider-First Engineered™, la nueva
        Tarmac es la culminación de nuestra insistente búsqueda de la velocidad…
      </p>
      <div id="cesta_compra">
      <compra></compra>
      </div>
      <div id="video">
        <iframe width="600" height="300" src="https://www.youtube.com/embed/-Y5fopNq5Lg" 
        title="YouTube video player" 
        frameborder="0" 
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
        allowfullscreen></iframe>
      </div>
    </div>
  </div>
  <div id="compra">
    <div id="fotos">
      <a @click="cambiarFoto(1)"
        ><img v-bind:src="bicis[1]" alt="Specialized S-Work vista 1" copyright="www.specialized.com"
      /></a>
      <a @click="cambiarFoto(2)"
        ><img v-bind:src="bicis[2]" alt="Specialized S-Work vista 2" copyright="www.specialized.com"
      /></a>
      <a @click="cambiarFoto(3)"
        ><img v-bind:src="bicis[3]" alt="Specialized S-Work vista 3" copyright="www.specialized.com"
      /></a>
      
    </div>
    
    
  </div>
</template>

<script>
import Compra from './Compra.vue'
export default {
components:{
  Compra
},
  data() {
    return {
      bicis: [
        require("../assets/bici-1.png"),
        require("../assets/bici-1.png"),
        require("../assets/bici-2.png"),
        require("../assets/bici-3.png"),
        require("../assets/logo.png"),
      ]
    };
  },

  methods: {
    cambiarFoto(id) {
      this.bicis[0] = this.bicis[id];
    }
  }
}
</script>

<style scopded>
#descripcion {
  display: flex;
  flex-direction: column;
  padding: 10px;
}
#descripcion p {
  font-size: 1.5em;
}
#foto {
  display: flex;
  margin-top: 40px;
}
#foto_principal{
  max-width: 1030px;
}
#fotos {
  display: flex;
  margin-top: 30px;
}
#fotos img {
  max-height: 200px;
}
#video{
  margin-left: 120px;
}

</style>


