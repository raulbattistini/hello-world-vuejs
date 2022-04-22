<template>
<div>
    <h2> Esta é a descrição da pessoa: {{ nome }}  </h2>
    <info1 :email="email" :esta_trabalhando=true />
    <Form />
</div>
</template>
<script>
import info1 from './info1.vue'
import Form from './Form.vue'
    export default {
        name: 'Pessoa',
        components: { 
            info1,
            Form, 
      },
        data(){
            return {
                nome: 'Raul',
                email: "raul@email.com",
            }
        }
    }
</script>