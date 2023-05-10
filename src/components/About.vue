<script>
export default {
    props: {
        src: String,
        titulo: String,
        text: String
    }
}
</script>

<template>
    <div class="container">
        <div class="card">
            <img class="imagem" :src="src" alt="">

            <h2 class="titulo"> {{ titulo }} </h2>

            <p class="text"> {{ text }}</p>
        </div>
    </div>
</template>

<style scoped>

.card {
    max-width: 25vw;
    padding: 3.7rem 2rem;
}

.imagem {
    padding-bottom: 3.7rem;
}

.titulo {
    padding-bottom: 1.25rem;
}



</style>
