<template>
  <div id="app">
    <Caixas @addTarefa="adicionarTarefa($event)"/>
    <lista :tarefas="tarefas"/>
  </div>
</template>

<script>
import Caixas from "./components/Caixas.vue"
import lista from "./components/lista.vue"

export default {
  name: 'App',
  components: {
    Caixas, lista
  }, data:function(){
    return{
        tarefas:[
        {descricao:"Química"},
        {descricao:"Sociologia"},
        {descricao: "Matemática"}
      ]
    }
  },
  methods:{
    adicionarTarefa: function(event){
      this.tarefas.push({descricao: event.novaTarefa})
    }
   }
}
</script>

<style>
</style>
