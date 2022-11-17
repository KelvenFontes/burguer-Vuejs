<template>

    <div>

        <Header />
        <PrimeiroComponente />
        <p class="paragrafo-pai">o dado do app é: {{testando}}</p>
        <Life-cycle />
        <Pessoa />

    </div>
  
</template>

<script>

    import Header from './components/Header.vue'
    import PrimeiroComponente from './components/PrimeiroComponente.vue'
    import LifeCycle from './components/LifeCycle.vue'
    import Pessoa from './components/Pessoa.vue'

    export default {
        name: 'App',
        components: {
            Header,
            PrimeiroComponente,
            LifeCycle,
            Pessoa
        },
        data(){
            return {
                testando: 'teste'
            }
        }
    }

</script>

<style>

    body{
        background-color: #333;
        color: #fff;
    }

    a {
        color: red;
    }

    .teste{
        background-color: #000;
    }

</style>