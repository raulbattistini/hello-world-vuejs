<template> 
<div>
  <Header :esta_logado="true" />
  <primeiroComponente1 />
  <p class="paragrafo-pai"> O dado de app é {{ testando }} </p>
  <lifeCycleHooks />
  <Pessoa />
  <info1 />
</div>
</template>

<script>
import Header from './components/header.vue';
import primeiroComponente1 from './components/PrimeiroComponente1.vue'
import lifeCycleHooks from './components/lifeCycleHooks.vue';
import Pessoa from './components/Pessoa.vue';
import info1 from './components/info1.vue';
export default {
  name: 'App',
  components: {
    primeiroComponente1,
    lifeCycleHooks,
    Pessoa,
    info1,
    Header,
    },
    data(){
      return{
        testando: "teste"
      }
    }
}
</script>
<style>
body{
  background-color: #15202B;
  color: #fff;
  font-family: Arial;
  font: 100;
}
h2{
  font-size: 20px;
}
p{
  font-size: 15px;
}
a{
  color: red;
}
.teste{
  background-color: #000;
}
</style>
