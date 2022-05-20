<template>
    <div>
        <p v-if="esta_trabalhando">Trabalhando no momento</p>
        <p v-else>Em busca de emprego</p>
        <p>Hard Skills:</p>
        <ul>
            <li v-for="(item, index) in hardSkills" v-bind:key="index">{{ item }}</li>
        </ul>
        <p>Soft Skills</p>
        <ul>
            <li v-for="item in softSkills" v-bind:key="item.id">
                {{ item.soft_skill }}
            </li>
        </ul>

        <div>
            <button @click.prevent="showEmail">{{ textoBotao }}</button>
        </div>

        <!-- .. Lembrando que v-show SEMPRE monta o elemento, apenas altera para display:none. v-if apenas se for true ;)-->
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
        <p>Meu portifólio <a v-bind:href="meu_link" target="_blank">Clique aqui</a></p>
        <Picture />
    </div>
</template>

<script>
import Picture from './Picture.vue'
    export default {
    components: { Picture },
        name: 'Info',
        data() {
            return {
                esta_trabalhando: false,
                mostrar_email: false,
                email: 'email@email.com',
                meu_link: 'https://google.com',
                textoBotao: 'Mostrar email',
                hardSkills: ['PHP','JavaScript','MYSQL'],
                softSkills: [
                    {id: 1, soft_skill: 'Boa comunicação'},
                    {id: 2, soft_skill: 'Trabalho em equipe'},
                    {id: 3, soft_skill: 'Inteligência emocional'}
                ]
            }
        },
        methods: {
            showEmail() {
                this.mostrar_email = !this.mostrar_email
                if(!this.mostrar_email) {
                    this.textoBotao = 'Mostrar email';
                } else {
                    this.textoBotao = 'Ocultar email'
                }
            }
        }
    }
</script>