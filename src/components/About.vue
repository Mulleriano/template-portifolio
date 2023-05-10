<script>
import about1 from '../assets/about/about1.svg'
import about2 from '../assets/about/about2.svg'
import about3 from '../assets/about/about3.svg'

export default {
    data() {
        return {
            cards: [
                {
                    src: about1,
                    alt: "about1"
                },
                {
                    src: about2,
                    alt: "about2"
                },
                {
                    src: about3,
                    alt: "about3"
                },
            ]
        }
    },
    props: {
        titulo: String,
        text: String
    }
}
</script>

<template>
    <div class="container">
        <div class="cards" v-for="card in cards">
            <img class="imagem" :src="card.src" :alt="card.alt">

            <h2 class="titulo"> {{ titulo }} </h2>

            <p class="text"> {{ text }}</p>
        </div>
    </div>
</template>

<style scoped>
.container {
    display: flex;
    justify-content: space-evenly;
    text-align: center;
    padding: 5rem 0;
}

.cards {
    max-width: 20vw;
    padding: 3.7rem 2rem;
}

.imagem {
    padding-bottom: 3.7rem;
}

.titulo {
    padding-bottom: 1.25rem;
}



</style>
