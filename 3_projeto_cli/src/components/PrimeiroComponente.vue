<template>
    <div>
        <h1>Componente Vue 3</h1>
        <p>Meu nome é: {{ nome }} e trabalho como {{ profissao }}</p>
        <MultiplosEventos />
        <Reutilizacao />
    </div>
</template>

<script>
    import MultiplosEventos from './MultiplosEventos.vue'
    import Reutilizacao from './Reutilizacao.vue'

    export default {
        name: 'PrimeiroComponente',
        components: {
            MultiplosEventos,
            Reutilizacao
        },
        data() {
            return {
                nome: 'Leonardo',
                profissao: 'Desenvolvedor'
            }
        }
    }
</script>