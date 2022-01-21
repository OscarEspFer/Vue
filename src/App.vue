<template>
  <div>
    <tabla-personas v-bind:persinas="personas"/>
    <targetes v-bind:persinas="personas"/>
    <formulario-persona/>
  </div>
  
</template>

<script>
import Targetes from '@/components/Targetes.vue'
import TablaPersonas from './components/TablaPersonas.vue'
import FormularioPersona from '@/components/FormularioPersona.vue'

export default {
  name: 'app',
  components: {
    Targetes,
    TablaPersonas,
    FormularioPersona,
  },
  data() {
    return {
      personas: [
        {
          id: 1,
          nombre: 'Jon',
          apellido: 'Aserje',
          email: 'jon@email.com',
        },
        {
          id: 2,
          nombre: 'Tyrion',
          apellido: 'Lannister',
          email: 'tyrion@email.com',
        },
        {
          id: 3,
          nombre: 'Daenerys',
          apellido: 'Targaryen',
          email: 'daenerys@email.com',
        },
        {
          id: 4,
          nombre: 'Oscar',
          apellido: 'España Ferrer',
          email: 'email@email.com',
        },
      ],
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
