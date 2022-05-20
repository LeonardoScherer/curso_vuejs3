<template>
    <div>
        <p v-if="esta_trabalhando">Trabalhando no momento</p>
        <p v-else>Em busca de emprego</p>
        <p>Hard Skills:</p>
        <ul>
            <li>PHP</li>
            <li>JavaScript</li>
            <li>MYSQL</li>
        </ul>
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
                mostrar_email: true,
                email: 'email@email.com',
                meu_link: 'https://google.com'
            }
        }
    }
</script>