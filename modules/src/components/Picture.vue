<template>
    <!-- Pode colocar apenas os : que ele já entende que é o v-bind -->
    <img :src="avatar" :alt="descricao">    
</template>

<script>
 
    export default {
        name: 'Picture',
        data() {
            return {
                // toda vez que coloca apenas /  ele já acessa a pasta public
                avatar: '/img/teste.png',
                descricao: 'Imagem do github'
            }
        }
    }

</script>
