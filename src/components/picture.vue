<template>
    <div>
<img :src="avatar" :alt="descricao">
<mudarimagem @mudarimagem="trocarimagem" />
    </div>
</template>
<script>
import mudarimagem from './mudarimagem.vue'
export default {
    name: 'Picture',
    components: {
        mudarimagem
        },
    data(){
        return{
            avatar: "/img/avatar.png",
            descricao: "Raul Battistini",
        }
    },
    methods:{
        trocarimagem(){
            this.avatar = '/img/avatar2.png'
        }
    }
}
</script>