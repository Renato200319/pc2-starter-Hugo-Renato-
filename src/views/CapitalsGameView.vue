<script>
import countries from "/src/datasets/countries.json";
import CountryComponent from "../components/CountryComponent.vue";

export default {
  name: "CapitalsGameView",
  components: {
    CountryComponent,
  },
  data() {
    return {
      country: {},
      capital: "",
      puntaje: 0,
    };
  },
  created() {
    this.country = countries[Math.floor(Math.random() * countries.length)];
  },
  methods: {
    setCapital(e) {
      //TODO: implementar. fija la capital del input.
    },
    adivinarCapital() {
      if(adivinanza == country.capital)
      puntaje = punataje+1
      //TODO: implementar. verifica se la adivinanza es correcta.
    },
  },
};
</script>

<template>
  <h1>Puntaje: {{ puntaje }}</h1>
  <div class="countries">
    <!-- TODO: usar los metodos definidos arriba dentro del input para llenar el estado de la capital a adivinar-->
    <input
      placeholder="Adivina la capital"
    />
    <button @click="adivinarCapital">Adivina!</button>
    <div class="countries-container">
      <div class="country" @click="clickeable ? $emit('click') : null">
    <img
      width="200"
      
      height="200"

      :src="`https://countryflagsapi.com/png/${code}`"
    />
    <h1> {{ name }}</h1>
    <h2>
      capital: {{ capital }}
    </h2>
    <h3>
      moneda: {{ currency_name }} ({{ currency }})
    </h3>
    <h3>
      region: {{ region }}
    </h3>
  <!--TODO: Poblar el HTML con las propiedades. Usar https://countryflagsapi.com/png/${code}-->
  <img
      width="200"
      height="200"
    />
  </div>
      <!--TODO: CREAR EL COMPONENTE PARA VISUALIZAR EL PAIS-->
    </div>
  </div>
</template>

<style scoped>
@media (min-width: 1024px) {
  .countries {
    align-items: center;
  }

  input {
    line-height: 2em;
  }

  .countries-container {
    margin-left: 35%;
    align-items: center;
    overflow-y: auto;
    vertical-align: middle;
    padding: 10px;
  }
}
</style>
