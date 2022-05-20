<template>
    <div>
        <p v-if="esta_trabalhando">Trabalhando no momento</p>
        <p v-else>Em busca de emprego</p>
        <p>Hard Skills:</p>
        <ul>
            <li>
                PHP
            </li>
            <li>
                JavaScript
            </li>
            <li>
                MYSQL
            </li>
        </ul>
        <!-- .. Lembrando que v-show SEMPRE monta o elemento, apenas altera para display:none. v-if apenas se for true ;)-->
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
    </div>
</template>

<script>
    export default {
        name: 'Info',
        data() {
            return {
                esta_trabalhando: false,
                mostrar_email: true,
                email: 'email@email.com'
            }
        }
    }
</script>