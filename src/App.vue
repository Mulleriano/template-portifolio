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
    position: fixed;
    top: 0;
    width: 100vw;
    z-index: 1;
    height: 10vh;
    padding: 0 3rem;

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
    padding: 0 5vw;
  }

  @media screen and (max-width: 600px) {
    header {
      justify-content: center;
    }
    nav{
      display: none;
    }

    main {
      padding: 0 1.5rem;
    }
  }
</style>
