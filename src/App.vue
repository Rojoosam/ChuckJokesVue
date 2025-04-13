<template>
  <div id="app">
    <h1>Chistes de Chuck Norris</h1>
    <ul>
      <li v-for="(chiste, index) in chuck" :key="index">
        {{ chiste.value }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      chuck: [
        { value: "Chuck Norris puede saltar en paracaídas al espacio exterior." },
        { value: "El principal producto de Chuck Norris es el dolor." },
        { value: "Chuck Norris no lee libros. Los mira fijamente hasta que obtiene la información que quiere." },
        { value: "El tiempo no espera a nadie. A menos que ese hombre sea Chuck Norris." },
        { value: "Si escribes Chuck Norris en Scrabble, ganas. Para siempre." }
      ]
    };
  }
};
</script>

<style scoped>
/* Estilos para darle un aspecto atractivo */
#app {
  text-align: center;
  margin: 20px;
  font-family: 'Arial', sans-serif;
  color: #333;
}

h1 {
  color: #2c3e50;
  margin-bottom: 20px;
}

ul {
  list-style: none;
  padding: 0;
  max-width: 600px;
  margin: 0 auto;
}

li {
  background: #ecf0f1;
  padding: 15px;
  margin-bottom: 10px;
  border-radius: 5px;
  transition: background 0.3s ease;
}

li:hover {
  background: #bdc3c7;
}
</style>
