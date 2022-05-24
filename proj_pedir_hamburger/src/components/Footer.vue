<template>
    <div id="footer">
        <p>Peça seu hamburger &copy; 2022</p>
    </div>
</template>

<script>
export default {
    name: 'Footer'
}
</script>

<style scoped>
    #footer {
        height: 200px;
        background-color: #222;
        border-top: 4px solid #111;
        color: #FCBA04;
        display: flex;
        align-items: center;
        justify-content: center;
        bottom: 0;
        width: 100%;
        position: absolute;
    }
</style>