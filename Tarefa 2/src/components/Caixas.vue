<template>
  <div id="Caixas">
  <input id="texto" type="text" placeholder="Adicionar Tarefa" v-model="novaTarefa">
  <button id="botao" @click="adicionarTarefa">Aplicar</button>
  </div>
</template>

<script>

export default {
    name: "Caixas",
    data: function(){
        return{
            novaTarefa: ''
        }

    }, methods:{
        adicionarTarefa: function(){
            this.$emit('addTarefa',{novaTarefa: this.novaTarefa})

        }
    }
}
</script>

<style>

    #Caixas{
        background-color: white;
        width: 500px;
        height: 200px;
        margin: 80px 0px 0px 35%;
        border: 2px black solid;
        
    }

    #texto{
        margin: 90px 0 0 27%;
        height: 25px;
        width: 200px;
        border: black 2px solid;
    }

    #botao{
       width: 60px;
       height: 30px;
       color: black;
       outline: none;
       cursor: pointer;
       margin: 0px 5px;
       border: 2px solid black;
    }
</style>