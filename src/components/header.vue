<template>
    <div>
        <ul>
            <li><a href="http://" target="_blank" rel="noopener noreferrer">Home</a></li>
            <li><a href="http://" target="_blank" rel="noopener noreferrer">Projetos</a></li>
            <li><a href="http://" target="_blank" rel="noopener noreferrer">Contato</a></li>
            <li v-if="esta_logado"> <a href="#" target="_blank"> Meu Perfil </a></li>
        </ul>
    </div>
</template>
<script>
export default {
    name: 'Header',
    props: ["esta_logado"],
}
</script>
<style scoped>
ul{
    list-style: none;
    display: flex;
    background-color: #aaa;
}
li{
    margin-right: 10px;

}
a{
    color: #fff;
    text-decoration: none;
    transition: .5s;
}
a:hover{
    color: turquoise;
}
</style>