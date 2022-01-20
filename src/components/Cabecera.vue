<template>
    <section id="cabecera">
        <div id="titulo">
            <h2 id="titulo_1">LUCKY</h2><h2 id="titulo_2">BIKE</h2>
        </div>
        <div id="menu">
            <div id="d_botones">
            <button class="botones" v-for="(valor,index) of menu" :key="index"><b>{{valor}}</b></button>
            </div>
            <div id="registros">
            <button class="registro" v-for="(valor2,index2) of registro" :key="index2">{{valor2}}</button>
            </div>
        </div>
    </section>
    
</template>

<script>
export default {
name: 'lista',
data(){
    return{
        menu:['CARRETERA','MONTAÑA','ACCESORIOS','COMPONENTES'],    
        registro:['REGISTRO','INICIAR SESIÓN']
    }
}
}
</script>

<style scoped>

#cabecera{
    display: flex;
    flex-direction: column;
    padding-left: 100px;
    background-color: rgba(0, 0, 0, 0.726);
}
#titulo{
    display: flex;
}
#titulo_1{
    color: white;
    font-size: 2em;
}
#titulo_2{
    color: red;
    font-size: 2em;
}
#menu{
    display: flex;
    border-radius: 0;
}
#d_botones{
    flex-basis: 70%;
    margin-bottom: 40px;
}
.botones{
    flex-basis: 300px;
    padding: 1em;
    border: solid black 2px;
    background-color: rgb(202, 9, 9);
    font-size: 1em;
}
.botones:hover{
    background-color: white;
}
#registros{
    flex-basis: 30%;
}
.registro{
    padding: 1em;
    font-size: 1em;
    background-color: white;
    flex-basis: 200px;
    border: solid black 2px;
}
.registro:hover{
    background-color: red;
}

</style>

