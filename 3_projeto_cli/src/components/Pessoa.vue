<template>
    <div>
        <h2>Informações sobre: {{ nome }}</h2>
        <Info :email="email" :esta_trabalhando="esta_trabalhando" />
        <Form />
    </div>
</template>

<script>
    import Form from './Form.vue'
    import Info from './Info.vue'

    export default {
        components: { Info, Form },
        name: 'Pessoa',
        data() {
            return {
                nome: 'Creusa',
                email: 'mail@mail.com',
                esta_trabalhando: true
            }
        }
    }
</script>