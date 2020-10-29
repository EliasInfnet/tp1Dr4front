<template>
  <div id="app">
    <b-list-group class="divTarefa" v-for="tarefa in tarefas" :key="tarefa.id">
      <b-list-group-item ><tarefa :id="tarefa.id" :descricao="tarefa.descricao" :estaCompleta="tarefa.estaCompleta"/></b-list-group-item>  
    </b-list-group>
  </div>
</template>

<script>
import Tarefa from './components/Tarefa.vue'
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

export default {
  name: 'App',
  data(){
    return{
      tarefas: 
      [{id: 1,descricao: "Tarefa1", estaCompleta:false},
       {id: 2,descricao: "Tarefa2", estaCompleta:true},
       {id: 3,descricao: "Tarefa3", estaCompleta:false},
       {id: 4,descricao: "Tarefa4", estaCompleta:true},
       {id: 5,descricao: "Tarefa5", estaCompleta:true}]
    }
  },
  components: {
    Tarefa
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
  margin: 60px;
  display: flex;
}

.divTarefa{
  margin-right: 40px;
}
</style>
