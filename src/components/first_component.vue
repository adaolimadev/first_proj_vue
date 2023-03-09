<template>
    <div>
        <h1>Utilizando o primeiro componente!</h1>
        <MultiplosEventos />
    </div>
    
</template>

<script>
import MultiplosEventos from './MultiplosEventos.vue'
    export default{
        name: 'first_component',
        components:{
            MultiplosEventos
        },
        data(){
            return {
                nome: "Adão Lima"
            }
        }
    }
</script>