<script>
import Form from './Form.vue';
export default {
    components: {
        Form,
    }
}
</script>

<template>
    <div class="container">
        <div class="content">
            <h2>Lets work together</h2>
            
            <p>This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com</p>
            
            <div class="redesSociais">
                <img src="../assets/contact/behance.svg" alt="Behance">
                <img src="../assets/contact/discord.svg" alt="Behance">
                <img src="../assets/contact/dribble.svg" alt="Behance">
                <img src="../assets/contact/facebook.svg" alt="Behance">
                <img src="../assets/contact/instagram.svg" alt="Behance">
            </div>
        </div>
        <Form />
    </div>


</template>

<style scoped>
.container {
    display: flex;
    justify-content: space-between;
}

.content {
    width: 30%;
}

h2 {
    font-size: 2rem;
    margin-bottom: 2rem;
}

.redesSociais {
    display: flex;
    align-items: center;
    margin-top: 3rem;
}
.redesSociais img {
    width: 2rem;
    margin-right: 1rem;
}

</style>