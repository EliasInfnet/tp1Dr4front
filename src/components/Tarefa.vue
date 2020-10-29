<template>
    <div>            
        <b-list-group-item>id : {{id}}</b-list-group-item>
        <b-list-group-item>descricao : {{descricao}}</b-list-group-item>
        <b-list-group-item variant="success" v-if="estaCompleta">A tarefa esta completa</b-list-group-item>
        <b-list-group-item variant="danger" v-else>A tarefa não esta completa</b-list-group-item>
    </div>    
</template>

<script>



import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

export default {
    props: {
        id:Number,
        descricao:String,
        estaCompleta:Boolean
    }
}
</script>

<style>
</style>


