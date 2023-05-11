<script>
import LogosSection from "../components/LogosSection.vue";
import About from "../components/About.vue";
import ListaAbout from "../components/ListaAbout.vue";
import Works from "../components/Works.vue";
import ListaWorks from "../components/ListaWorks.vue";
import Clients from "../components/Clients.vue";
import ListaClients from "../components/ListaClients.vue";
import Contact from "../components/Contact.vue";

export default {
  components: {
    LogosSection,
    About,
    ListaAbout,
    Works,
    ListaWorks,
    Clients,
    ListaClients,
    Contact,
  },
};
</script>

<template>
  <section id="hero">
    <div class="heroContent">
      <p class="branding bold">Branding | Image Making</p>
      <h1 class="bold">
        Visual <br />
        Designer
      </h1>

      <p>
        This is a template Figma file, turned into code using Anima. Learn more
        at AnimaApp.com
      </p>
    </div>

    <div class="heroImg">
      <img src="../assets/hero.png" alt="Hero" />
    </div>
  </section>

  <section id="logos">
    <LogosSection />
  </section>

  <section id="about">
    <ListaAbout />
  </section>

  <section id="works">
    <ListaWorks />
  </section>

  <section id="clients">
    <ListaClients />
  </section>

  <section id="contact">
    <Contact />
  </section>
</template>

<style scoped>
/* Estilo do Hero */
#hero {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
  height: 84vh;
  padding: 0 5rem;
}

.heroContent {
  width: 50%;
}

h1 {
  font-size: 6rem;
  padding: 3rem 0;
  font-weight: 600;
}

.branding {
  font-size: 1.25rem;
}

.heroImg {
    width: 50%;
    display: flex;
    justify-content: flex-end;
}

#logos,
#about,
#works,
#clients,
#contact {
  padding: 4rem 0;
}

@media screen and (max-width: 600px) {
  #hero {
    flex-direction: column;
    justify-content: center;
    padding: 10vh 0;
    text-align: center;
    height: auto;
  }
  .heroContent {
    width: auto;
  }
  h1 {
    font-size: 4rem;
  }
  .heroImg {
    width: 100%;
    padding-top: 7vh;
  } 
}
</style>
