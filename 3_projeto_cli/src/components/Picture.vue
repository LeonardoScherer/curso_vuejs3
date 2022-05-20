<template>
    <img :src="avatar" :alt="descricao" class="img">
</template>

<script>
    export default {
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