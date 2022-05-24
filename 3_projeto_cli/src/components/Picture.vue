<template>
    <div>
        <img :src="avatar" :alt="descricao" class="img">
        <MudarImagem @mudar-imagem="trocarImagem"/>
    </div>
</template>

<script>
    import MudarImagem from './MudarImagem.vue'
    
    export default {
        components: { MudarImagem },
        name: 'Picture',
        data() {
            return {
                avatar: "/img/profile.png",
                descricao: "Imagem de perfil"
            }
        },
        methods: {
            trocarImagem() {
                this.avatar = '/img/avatar2.png'
            }

        }
    }
</script>

<style scoped>
.img {
    width: 100px;
    height: 100px;
}
</style>