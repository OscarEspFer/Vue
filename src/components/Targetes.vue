<template>
    <div id="targetes">
        <button v-on:click="funcio()">Mostrar/Ocultar Targetes</button>
        <div v-if="boto">
            <div class="card" style="width:200px; display:inline-block; " v-for="persona in persinas" v-bind:key="persona.id" >
                <img class="card-img-top" src="../assets/logo.png" alt="Card image">
                <div class="card-body">
                    <h4 class="card-title">{{ persona.nombre }}</h4>
                    <p class="card-text">{{ persona.email }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
  export default {
    name: 'targetes',
    props: {
        persinas: Array,
    },
    methods:{
        funcio(){
            this.boto = !this.boto
        }
    },
      /* ✓ GOOD */
    data () {
        return {
        boto: false
        }
    }

  }
</script>

<style scoped></style>