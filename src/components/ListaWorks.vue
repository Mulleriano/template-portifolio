<script>
import work1 from '../assets/works/works1.png';
import work2 from '../assets/works/works2.png';
import work3 from '../assets/works/works3.png';
import work4 from '../assets/works/works4.png';
import work5 from '../assets/works/works5.png';
import work6 from '../assets/works/works6.png';

import Works from './Works.vue';

export default {
    components: {
        Works
    },
    data() {
        return {
            works: [
                {
                    src: work1,
                    titulo: "Project Title",
                    text: "UI, Art direction"
                },
                {
                    src: work2,
                    titulo: "Project Title",
                    text: "UI, Art direction"
                },
                {
                    src: work3,
                    titulo: "Project Title",
                    text: "UI, Art direction"
                },
                {
                    src: work4,
                    titulo: "Project Title",
                    text: "UI, Art direction"
                },
                {
                    src: work5,
                    titulo: "Project Title",
                    text: "UI, Art direction"
                },
                {
                    src: work6,
                    titulo: "Project Title",
                    text: "UI, Art direction"
                }
            ]
        }
    }
}

</script>
<template>
    <div class="container">
        <h2>Latest work</h2>
        <div class="projects">
            <div v-for="work in works">
                <Works :src="work.src" :titulo="work.titulo" :text="work.text" />
            </div>
        </div>
    </div>
</template>

<style scoped>
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
}

h2 {
    text-align: center;
    font-size: 2rem;
    padding: 3rem 0 5rem 0;
}

.projects {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    column-gap: 8vw;
    row-gap: 5vh;
}

</style>
