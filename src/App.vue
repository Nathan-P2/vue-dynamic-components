<template>
  <div>
    <button @click="componenteAtivo = 'Sobre'">Sobre</button>
    <button @click="componenteAtivo = 'Servicos'">Servicos</button>
    <button @click="componenteAtivo = 'Formulario'">Formulario</button>
    <keep-alive>
      <component :is="componenteAtivo"></component>
    </keep-alive>
  </div>
</template>

<script>
import Sobre from './components/Sobre.vue'
import Servicos from './components/Servicos.vue'
import Formulario from './components/Formulario.vue'
  export default {
    components: {
      Sobre,
      Servicos,
      Formulario
    },
    data() {
      return {
        componenteAtivo: ''
      }
    }
  }
</script>

<style scoped>

</style>