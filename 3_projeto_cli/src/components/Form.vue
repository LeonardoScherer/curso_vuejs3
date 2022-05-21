<template>
    <form action="" @submit.prevent="enviarFormulario">
        <div>
            <input type="text" v-model="name" placeholder="Nome">
        </div>
        <div>
            <input type="email" v-model="email" placeholder="Email">
        </div>
        <div>
            <Submit />
        </div>
    </form>
</template>

<script>
    import InputText from './form/InputText.vue'
    import Submit from './form/Submit.vue'
    export default {
        name: 'Form',
        components: {
            InputText,
            Submit
        },
        data() {
            return {
                name: "",
                email: ""
            }
        },
        methods:  {
            enviarFormulario() {

                const name = this.name;
                const email = this.email;

                console.log(name, email);
            }
        }
    }
</script>