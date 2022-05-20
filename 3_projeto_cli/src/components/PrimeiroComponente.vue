<template>
    <div>
        <h1>Componente Vue 3</h1>
        <p>Meu nome é: {{ nome }} e trabalho como {{ profissao }}</p>
    </div>
</template>

<script>
    export default {
        name: 'PrimeiroComponente',
        data() {
            return {
                nome: 'Leonardo',
                profissao: 'Desenvolvedor'
            }
        }
    }
</script>