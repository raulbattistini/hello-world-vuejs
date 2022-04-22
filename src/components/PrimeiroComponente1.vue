<template>
<div>
  <h1>Hello Vue!</h1>
  <p>Meu nome é {{ nome }} e trabalho como {{ profissao }}</p>
  <multiploseventos />
  <reutilizacao />
</div>
</template>
<script>
import multiploseventos from './multiploseventos.vue'
import reutilizacao from './reutilizacao.vue'

export default {
  name: 'primeiroComponente1',
  components:{
    multiploseventos,
    reutilizacao,
  },
  data(){
    return{
      nome: "Raul", 
      profissao: "none",
    }
  }
}
</script>