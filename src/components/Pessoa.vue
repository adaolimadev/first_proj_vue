<template>
    <div>
        <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
       <Info compEmail="props@mail.com"/>
       <Form />
    </div>
</template>

<script>
    import Info from './info'
    import Form from './Form.vue'
    export default{
        name: 'Pessoa',
        components:{
            Info,
            Form
        },
        data(){
            return{
                nome: 'Adao'
            }
        }
    }
</script>