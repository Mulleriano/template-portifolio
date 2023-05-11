<script>
export default {
  props: {
    src: String,
    titulo: String,
    text: String,
  },
};
</script>

<template>
  <div class="container">
    <div class="card">
      <img class="imagem" :src="src" alt="" />

      <h3 class="titulo">{{ titulo }}</h3>

      <p class="text">{{ text }}</p>
    </div>
  </div>
</template>

<style scoped>
.card {
  max-width: 24vw;
  padding: 3.7rem 2rem;
}

.imagem {
  padding-bottom: 3.7rem;
}

.titulo {
  padding-bottom: 1.25rem;
  font-size: 1.6rem;
  font-weight: 600;
}
</style>
