<template>
    <div id="main-banner">
        <h1>Peça seu hamburger</h1>
    </div>
</template>

<script>
export default {
    name: 'Banner'
}
</script>

<style scoped>

    #main-banner {
        background-image: url('/public/img/burger.jpg');       
        background-position: 0 -250px;
        height: 800px;
        justify-content: flex-start;
        align-items: center;
        display: flex;
    }

    #main-banner h1 {
        color: #FFF;
        text-align: center;
        font-size: 60px;
        background-color: #222;
        padding: 20px;

    }
     
</style>