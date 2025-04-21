<template>
  <div id="app">
    <h1>Chistes de Chuck Norris</h1>
    <div class="container">
      <div class="cards-container">
        <div
          v-for="(chiste, index) in chuck"
          :key="index"
          class="card-wrapper"
        >
          <chuck-card
            :icon_url="chiste.icon_url"
            :value="chiste.value"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ChuckCard from './components/ChuckCard.vue';

export default {
  name: "App",
  components: { ChuckCard },
  data() {
    return {
      chuck: [
        {
          icon_url: "img/chuck.jpg",
          value: "Chuck Norris puede saltar en paracaídas al espacio exterior."
        },
        {
          icon_url: "img/chuck2.jpg",
          value: "El principal producto de Chuck Norris es el dolor."
        },
        {
          icon_url: "img/chuck3.jpg",
          value: "Chuck Norris no lee libros. Los mira fijamente hasta que encuentra la información que busca."
        },
        {
          icon_url: "img/chuck4.jpg",
          value: "El tiempo no espera a nadie. A menos que ese hombre sea Chuck Norris."
        },
        {
          icon_url: "img/chuck.jpg",
          value: "Si deletreas Chuck Norris en Scrabble, ganas. Para siempre."
        }
      ]
    };
  }
};
</script>

<style scoped>
.container {
  max-width: 1200px;
  margin: 0 auto;
  text-align: center;
}
h1 {
  margin: 20px 0;
}

/* Flex-wrap container */
.cards-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1rem;
  padding: 1rem 0;
}

/* Cada tarjeta ocupa ~33% para que las 3 primeras queden en la 1ª fila */
.card-wrapper {
  flex: 0 0 calc(33.333% - 1rem);
  max-width: calc(33.333% - 1rem);
}

/* En pantallas medias: 2 por fila */
@media (max-width: 768px) {
  .card-wrapper {
    flex: 0 0 calc(50% - 1rem);
    max-width: calc(50% - 1rem);
  }
}

/* En móviles: 1 por fila */
@media (max-width: 576px) {
  .card-wrapper {
    flex: 0 0 100%;
    max-width: 100%;
  }
}
</style>
