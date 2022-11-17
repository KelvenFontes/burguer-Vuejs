<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Estou Desempregado</p>
        <p>Utilizo as seguintes Tecnologias: </p>
        <ul>
            <li>JavaScript</li>
            <li>PHP</li>
            <li>Python</li>
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
                meu_link: 'https://google.com'
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
