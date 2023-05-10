<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
  <header>
    <a class="bold" href="#">Logo</a>

    <nav>
      <a href="">About</a>
      <a href="">Work</a>
      <a href="">Contact</a>
    </nav>
  </header>

  <main>
    <RouterView />
  </main>
  
</template>

<style scoped>
  header {
    z-index: 1;
    height: 10vh;
    padding: 0 3rem;
    background-color: aqua;

    display: flex;
    justify-content: space-between;
    align-items: center;
    text-decoration: underline;
  }

  header > a {
    font-size: 1.3rem;
  }

  nav {
    width: 20%;
    display: flex;
    justify-content: space-between;
    font-size: 1rem;
  }

  main {
    height: 200vh;
    background-color: antiquewhite;
  }
</style>
