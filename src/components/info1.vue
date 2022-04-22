<template>
<div>
    <p v-if="esta_trabalhando"> Estou trabalhando no momento. </p>
    <p v-else> Estou buscando novas oportunidades. </p>
    <p> Utilizo as seguintes tecnologias para back-end: </p>
    <!-- <p> Saiba mais sobre em: </p> -->
    <ul>
        <li v-for="(technology, index) in backend_technologies" v-bind:key="index"> {{technology}} </li>
    </ul>
    <p>Utilizo as seguintes tecnologias para front-end: </p>
    <ul>
        <li v-for="technology in frontend_technologies" :key="technology"> {{technology.language}} </li>
    </ul>
    <div>
        <button @click="showEmail"> {{ textoBotao }} </button>
    </div>
    <p v-show="mostrar_email"> Mande uma mensagem para: {{ email }}</p>
    <p class="teste"> Para acessar meu portfolio <a target="_blank" v-bind:href="meu_link"> basta clicar aqui </a></p>
    <!-- <p v-if="4 < 2"> Testando </p> -->
    <Picture />
</div>    
</template>
<script>
import Picture from './picture.vue'

export default {
    name: 'info1', 
    components: { 
        Picture 
    },
    props:{
        email: String,
        esta_trabalhando: Boolean,
    },
    data(){
        return{
            mostrar_email: false,
            meu_link: 'https://google.com',
            textoBotao: 'Mostrar email',
            backend_technologies: ["Javascript", "PHP", "Python"],
            frontend_technologies: [
                {id: 1, language: 'HTML'},
                {id: 2, language: 'CSS'},
                {id: 3, language: 'Vue'},
            ]
        }
    },
    methods: {
        showEmail(){
            this.mostrar_email = !this.mostrar_email
            if(!this.mostrar_email){
                this.textoBotao = 'Mostrar email'
            } else {
                this.textoBotao = 'Esconder email'
            }
        }
    }
}
</script>
<style>
    .paragrafo-pai{
        color: #7856FF;
    }
</style>