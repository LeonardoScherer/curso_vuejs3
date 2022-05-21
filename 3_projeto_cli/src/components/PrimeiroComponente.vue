<template>
    <div>
        <h1>Componente Vue 3</h1>
        <p>Meu nome é: {{ nome }} e trabalho como {{ profissao }}</p>
        <MultiplosEventos />
    </div>
</template>

<script>
    import MultiplosEventos from './MultiplosEventos.vue'
    export default {
        name: 'PrimeiroComponente',
        components: {
            MultiplosEventos
        },
        data() {
            return {
                nome: 'Leonardo',
                profissao: 'Desenvolvedor'
            }
        }
    }
</script>