<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Estou Desempregado</p>
        <p>Utilizo as seguintes Tecnologias para back-end: </p>
        <ul>
            <li v-for="(technology, index) in backend_technologies" v-bind:key="index">{{ technology }}</li>
        </ul>
        <p>Utilizo as seguintes tecnologias para front-end: </p>
        <ul>
            <li v-for="technology in frontend_technologies" v-bind:key="technology.id">{{ technology.language }}</li>
        </ul>
        <div>
            <button @click="showEmail">mostrar e-mail</button>
        </div>
        <p v-show="mostrar_email">Mande um email para {{ email }}</p>
        <p class="teste">Para acessar meu portifolio <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a></p>
        <Picture />
    </div>
</template>

<script>
import Picture from './Picture.vue'

    export default {
        name: 'Info',
        components: {
            Picture
        },
        data() {
            return {
                esta_trabalhando: true,
                mostrar_email: false,
                email: 'kelvenbentofontes@gmail.com',
                meu_link: 'https://google.com',
                backend_technologies: ['JavaScript', 'PHP', 'Python', 'Java'],
                frontend_technologies: [
                    {id:1, language: 'html'},
                    {id:2, language: 'css'},
                    {id:3, language: 'javaScript'},
                    {id:4, language: 'Vue.js'}
                ]
            }
        },
        methods: {
            showEmail(){
                this.mostrar_email = !this.mostrar_email
            }
        }
    }

</script>

<style>

    .paragrafo-pai{
        color: rgb(255, 196, 0);
    }

</style>
