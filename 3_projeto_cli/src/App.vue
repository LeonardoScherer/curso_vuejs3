<template>
  <div>
    <Header />
    <PrimeiroComponente />
    <hr>
    <LifeCycle />
    <hr>
    <Pessoa />
    <hr>

    <!-- <div class="my-3">
      <DialogModal v-if="openDialog">
        <div><h1>Download em andamento</h1></div>
        <div>
          <p><b>Atenção:</b> este é um teste de modal</p>
        </div>
        <div>
          <button class="btn btn-primary" @click.prevent="openDialog = false">OK</button>
        </div>
      </DialogModal>
        <div>
          <button @click.prevent="onOpenDialog()" class="btn btn-primary">
            Abrir dialogo
          </button>
        </div>
    </div> -->
  </div>

</template>

<script>
  import PrimeiroComponente from './components/PrimeiroComponente.vue'
  import LifeCycle from './components/LifeCycle.vue'
  import Pessoa from './components/Pessoa.vue'
  import Header from './components/Header.vue'
  //import DialogModal from './components/DialogModal.vue'

  export default {
    name: 'App',
    data() {
      /* return {
        openDialog: false,
      } */
    },
    components: {
      PrimeiroComponente,
      LifeCycle,
      Pessoa,
      Header,
      /* DialogModal, */
    },
    methods: {
      /* onOpenDialog() {
        this.openDialog = true;
      } */
    },
  }
</script>

<style>
  body {
    background-color: #333;
    color: #fff;
  }
</style>