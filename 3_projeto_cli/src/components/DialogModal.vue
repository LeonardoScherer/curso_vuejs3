<template>
    <div>
        <div class="backdrop"></div>
            
        <div class="dialog">
            <slot></slot>
        </div>
    </div>
</template>

<style scoped>
.backdrop {
    background: rgba(0, 0, 0, 0.5);
    position: fixed;
    left: 0px;
    top: 0px;
    width: 100%;
    height: 100%;
}
.dialog {
    position: fixed;
    top: 20%;
    background: #fff;
    width: 60vw;
    left: 20vw;
    padding: 20px;
}
</style>

<script>
export default {
    name: 'DialogModal'
}
</script>
