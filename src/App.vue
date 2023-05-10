<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
  <header>
    <a href="#">Logo</a>

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
    background-color: aqua;
    height: 10vh;
    padding: 0 3rem;

    display: flex;
    justify-content: space-between;
    align-items: center;
    text-decoration: underline;
  }

  header > a {
    font-weight: 600; 
  }

  nav {
    width: 20%;
    display: flex;
    justify-content: space-between;
  }

  main {
    height: 120vh;
    padding-top: 10vh;
    background-color: antiquewhite;
  }
</style>
