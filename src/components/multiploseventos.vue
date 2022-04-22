<template>
<div>
    <h2>
        <button @click="primeiro(txt1, $event), segundo(txt2, $event), terceiro($event)"> Ativar multiplos eventos!!!</button>
        <p> {{multiplos_eventos}} </p>
    </h2>
</div>    
</template>
<script>
export default {
    name: 'multiploseventos',
    data(){
        return{
            multiplos_eventos: "",
            txt1: "Primeiro evento. (1) ",
            txt2: "Segundo evento. (2) ",
        }
    },
    methods:{
        primeiro(txt, e){
            this.multiplos_eventos = txt;
        },
        segundo(txt, e){
            setTimeout(() => this.multiplos_eventos = txt, 1000)
        },
        terceiro(e){
            setTimeout(() => this.multiplos_eventos = "", 2000)
        }
    },
}
</script>
<style scoped>
div, p{
    text-align: center;
}

</style>