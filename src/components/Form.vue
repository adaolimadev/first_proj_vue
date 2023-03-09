<template>
    <div>
        <h2>Formulario de cadastro</h2>
        <form action="" @submit.prevent="enviarForm">
            <div> <InputText /> </div>
            <div> <InputText /> </div>
            <div> <Submit /> </div>
        </form>
    </div>
</template>

<script>
import InputText from './form/input.vue'
import Submit from './form/submit.vue'
export default {
    name: 'Form',
    components:{
        InputText,
        Submit
    },
    methods:{
        enviarForm(){
            console.log("Formulario enviado!")
        }
    }
}
</script>