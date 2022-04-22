<template>
    <div>
        <h1>Meu nome é: {{ nome }} </h1>
    </div>
</template>
<script>
export default {
    name: "lifeCycleHooks",

data(){
    return{
        nome: "Ainda não sei"
    }
},
created(){
    setTimeout(()=> {
    this.nome = "Raul"    
    }, 2000);
    this.lifeCycle()
},
mounted(){
    setTimeout(() => {
     this.nome = "Pedro"   
    }, 2000);
    this.lifeCycle()
},
methods: {
    lifeCycle(){
        console.log("Executou")
       }
}
}

</script>