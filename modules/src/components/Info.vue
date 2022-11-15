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
        <p v-if="1 > 2">Testando </p>
    </div>
</template>

<script>

    export default {
        name: 'Info',
        data() {
            return {
                esta_trabalhando: true
            }
        }
    }

</script>
