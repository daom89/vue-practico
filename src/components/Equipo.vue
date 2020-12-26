<template>
  <b-card :header="info.nombre" :img-src="info.logo" img-alt="Equipos" style="max-width: 20rem;" class="mb-2">
    <b-card-text>
        Estado: <div :class="{'activo': info.estado, 'inactivo': !info.estado}" class="circulo"></div>
      <br>
      Jugadores: {{ info.jugadores.length }}
      <br>
      <b-button href="#" variant="primary">Ver Jugadores</b-button>
    </b-card-text>
  </b-card>
</template>

<script>
export default {
  props: {
    info: {
      nombre: String,
      logo: String,
      estado: Boolean,
      jugadores: Array
    }
  },
  data(){
    return {
      // nombre: "Equipo 1",
      // logo: "https://loremflickr.com/600/300/football",
      // estado: false,
      // jugadores: [{jugador: "1"}, {jugador: "2"}, {jugador: "3"}]
    }
  },
  name: "Equipo"
}
</script>

<style scoped>
.circulo {
  width: 20px;
  height: 20px;
  border-radius: 50%;
  margin: 0 auto;
}
  .activo {
    background-color: green;
  }
  .inactivo {
    background-color: gray;
  }
</style>