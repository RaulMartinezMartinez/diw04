<template>
      <div id="seleccion">
        <div id="botones">
            <button @click="sumaContador(1)" id="sumar">+</button>
            <input type="text" id="cantidad" :value="contador" />
            <button @click="sumaContador(-1)" id="restar">-</button>
        </div>
        <div id="d_cesta">
            <button v-show="ver" id="cesta">Añadir a la cesta</button>
        </div>
      </div>
</template>

<script>
export default {
data(){
    return{
        contador: 1,
        ver: true
    }
},
methods: {
    verCesta(contador){
        if (contador < 1) {
            this.ver = false
        }else{
            this.ver = true
        }
    },
    sumaContador(num){
        if ((isNaN(this.contador))) {
            this.contador = 0
        }else{
            this.contador = this.contador + num;
            if (this.contador < 0) {
                this.contador = 0
            }
        
        }
        this.verCesta(this.contador)
    }
}
}
</script>

<style scoped>
#seleccion{
    display: flex;
    justify-content: center;
    margin: 30px;
}
#botones{
    display: flex;
    flex-basis: 20%;
    margin: 10px;
}
#d_cesta{
    display: flex;
    flex-basis: 20;
    margin: 10px;
}
#cesta{
    font-size: 2em;
    background-color: rgb(202, 9, 9);
    border: solid white 2px;
}
#cesta:hover{
    background-color: white;
}
#cantidad{
    width: 2em;
    text-align: center;
}
#sumar{
    width: 40px;
    height: 4em;
}
#restar{
    width: 40px;
}
</style>