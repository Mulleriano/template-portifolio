<script setup>
import LogosSection from '../components/LogosSection.vue';
import About from '../components/About.vue';
import Works from '../components/Works.vue';
import Clients from '../components/Clients.vue';

</script>

<template>
    <section id="hero">
        
        <div class="heroContent">
            <p class="branding bold">Branding | Image Making</p>
            <h1 class="bold">
                Visual <br>
                Designer
            </h1>

            <p>
                This is a template Figma file, turned into code <br>
                using Anima. Learn more at AnimaApp.com
            </p>
        </div>

        <div class="heroImg">
            <img src="../assets/hero.png" alt="Hero">
        </div>

    </section>

    <section id="logos">
        <LogosSection />
    </section>

    <section id="about">
        <About titulo="Product Design" text="This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com"/>
    </section>

    <section id="works">
        <Works />
    </section>

    <section id="clients">
        <Clients />
    </section>

    <section id="contact">

    </section>

</template>

<style scoped>
/* Estilo do Hero */
#hero {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: center;
    height: 80vh;
}

h1 {
    font-size: 6rem;
    padding: 3rem 0;
    font-weight: 600;
}

.branding {
    font-size: 1.2rem;
}
/* Estilo da seção de logos */


</style>