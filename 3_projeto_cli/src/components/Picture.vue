<template>
    <div>
        <img :src="avatar" :alt="descricao" class="img">
        <Reutilizacao />
    </div>
</template>

<script>
    import Reutilizacao from './Reutilizacao.vue'
    export default {
        components: { Reutilizacao },
        name: 'Picture',
        data() {
            return {
                avatar: "/img/profile.png",
                descricao: "Imagem de perfil"
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