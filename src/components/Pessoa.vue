<template>
    <div>
        <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
       <Info />
    </div>
</template>

<script>
    import Info from './info'
    export default{
        name: 'Pessoa',
        components:{
            Info
        },
        data(){
            return{
                nome: 'Adao'
            }
        }
    }
</script>