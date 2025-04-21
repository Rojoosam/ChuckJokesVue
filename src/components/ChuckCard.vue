<template>
  <div class="card custom-card">
    <img :src="icon_url" class="card-img-top chuck-img" alt="Chuck Norris">
    <div class="card-body">
      <p class="card-text">{{ value }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ChuckCard',
  props: {
    icon_url: { type: String, required: true },
    value:    { type: String, required: true }
  }
};
</script>

<style scoped>
.card {
  transition: transform 0.2s;
  border: 1px solid rgba(0,0,0,0.125);
  border-radius: 0.25rem;
  overflow: hidden;
}
.card:hover {
  transform: translateY(-5px);
}

/* Contenedor fijo para las tarjetas */
.custom-card {
  width: 160px;
}

/* Imagen limitada dentro de la tarjeta */
.chuck-img {
  max-width: 100px;
  max-height: 100px;
  object-fit: contain;
  margin: 10px auto 0;
  display: block;
}

/* Texto ligeramente más pequeño */
.card-text {
  font-size: 0.85rem;
  text-align: center;
}
</style>
