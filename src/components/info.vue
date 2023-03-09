<template>
    
    <div>
        <Picture />
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Estou a procura de oportunidades</p>
        <p>utilizo as seguintes tecnologias:</p>
        <ul>
            <li>PHP</li>
            <li>Laravel</li>
            <li>VueJS</li>
            <li>Docker</li>
            <li>Git / GitHub</li>
        </ul>
        <p>Para Acessar meu github <a v-bind:href="meu_link" target="_blank">clique aqui</a></p>
        <div>
            <button @click="showEmail">{{textoBotao}}</button>
        </div>
        <p v-show="mostrar_email">Seu email é {{ email }}</p>
        
    </div>
</template>

<script>
import Picture from './Picture.vue'

export default {
    name:'Info',
    components:{
        Picture
    },
    data(){
        return {
            esta_trabalhando: false,
            meu_link: 'https://github.com/snakeg0d',
            email: 'adao@balfex.com.br',
            mostrar_email: false,
            textoBotao: 'Mostrar Email'
        }
    },
    methods:{
        showEmail(){
            this.mostrar_email = !this.mostrar_email
            if(!this.mostrar_email){
                this.textoBotao = 'Mostrar e-mail'
            }else{
                this.textoBotao = 'Ocultar e-mail'

            }
        }
    }
}
</script>