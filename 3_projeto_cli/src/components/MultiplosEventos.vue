<template>
    <div>
        <button @click="primeiro('Primeiro evento', $event), segundo($event), terceiro(txt3, event), quarto()">Ativar múltiplos métodos</button>
        <p>{{ multiplos_eventos }}</p>
    </div>
</template>

<script>
export default {
    name: 'MultiplosEventos',
    data() {
        return {
            multiplos_eventos: "",
            txt3: "Terceiro evento"
        }
    },
    methods: {
      primeiro(txt, event) {
        this.multiplos_eventos = txt
      },
      segundo(event) {
        setTimeout(() => this.multiplos_eventos = "Segundo evento", 1000)
      },
      terceiro(txt, event) {
        setTimeout(() => this.multiplos_eventos = txt, 1500)
      },
      quarto() {
        setTimeout(() => this.multiplos_eventos = "", 2000)
      }
    }

}
</script>

<style scoped>
    div {
        margin: 100px;
    }
</style>