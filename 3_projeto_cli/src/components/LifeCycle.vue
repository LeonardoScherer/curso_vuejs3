<template>
    <div>
        <h1>Nome: {{ nome }}</h1>
    </div>
</template>

<script>
    export default {
        name: 'LifeCycle',
        data() {
            return {
                nome: 'Fulano'
            }
        },
        created() {
            setTimeout(() => {
                this.nome = 'Ciclano'
            }, 1000);
            
            this.lifeCycle();
        },
        mounted() {
            setTimeout(() => {
                this.nome = 'Beltrano'
            }, 1500);

            this.lifeCycle();

        },
        methods: {
            lifeCycle() {
                console.log('executou');
            }
        }
    }
</script>