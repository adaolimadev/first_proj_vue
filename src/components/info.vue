<template>
    
    <div>
        <Picture />
        <p>{{ compEmail }}</p>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Estou a procura de oportunidades</p>
        <p>Utilizo as seguintes tecnologias:</p>
        <ul >
            <li v-for="tec, index in technologies" v-bind:key="index">
                {{ tec }}
            </li>
        </ul>
        <p>Desenvolvi os seguintes projetos:</p>
        <ul>
            <li v-for="proj in projects" :key="proj.id">
                Nome: {{ proj.nome }} /
                Linguagem: {{ proj.language }}
            </li>
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
    props:{
        compEmail: String
    },
    data(){
        return {
            esta_trabalhando: true,
            meu_link: 'https://github.com/snakeg0d',
            email: 'adao@balfex.com.br',
            mostrar_email: false,
            textoBotao: 'Mostrar Email',
            technologies: ['PHP', 'Laravel', 'VueJs', 'Docker', 'Git', 'MySQL'],
            projects: [
                {id: 1, nome: 'biblioteca', language: 'php+mysql'},
                {id: 2, nome: 'bibliotecav2', language: 'php+pdo+mysql'},
                {id: 3, nome: 'bibliotecav3', language: 'php+laravel+vue+mysql'}
            ]
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