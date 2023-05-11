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
  <img :src="src" alt="works" />
  <div class="project-text">
    <h3>{{ titulo }}</h3>
    <p>{{ text }}</p>
  </div>
</template>

<style scoped>
h3 {
  font-size: 1.2 rem;
  padding: 20px 0 10px;
}
</style>
