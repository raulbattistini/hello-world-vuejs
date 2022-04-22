<template>
    <div>
    <h2> Meu formulário: </h2>
<form action="" @submit="enviarFormulario($event)">
    <div> 
<input type="text" v-model="name">
    </div>
    <div> 
<input type="text" v-model="email">
    </div>
    <div> 
        <submit />
    </div>
</form>
    </div>
</template>
<script>
import inputtext from './form/inputtext.vue';
import submit from './form/submit.vue';
export default {
    name: 'Form',
    components: { 
    inputtext, submit 
    },
    data(){
        return{
        name: "",
        email: "",
        }
    },
    methods: {
        enviarFormulario(e){
            e.preventDefault();
            const name = this.name;
            const email = this.email;
            console.log('Formulário enviado!');
            console.log("O nome é: " + name);
            console.log("O email é: " + email);
//
        }
    }
}
</script>
<style>
p, h2, submit { text-align: center; } 

</style>