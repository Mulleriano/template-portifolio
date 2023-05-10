<script>
import adidas from '../assets/logos/adidas.png'
import apple from '../assets/logos/apple.png'
import google from '../assets/logos/google.png'
import intercom from '../assets/logos/intercom.png'
import nike from '../assets/logos/nike.png'
import samsung from '../assets/logos/samsung.png'

export default {
    data() {
        return {
            logos: [
                {
                    src: adidas,
                    alt: "Adidas"
                },
                {
                    src: apple,
                    alt: "Apple"
                },
                {
                    src: google,
                    alt: "Google"
                },
                {
                    src: intercom,
                    alt: "Intercom"
                },
                {
                    src: nike,
                    alt: "Nike"
                },
                {
                    src: samsung,
                    alt: "Samsung"
                }
            ]
        }
    }
}
</script>

<template>
    <div class="teste">
        <div class="logos" v-for="logo in logos">
            <img :src="logo.src" :alt="logo.alt">
        </div>
        
    </div>
</template>

<style scoped>
    .teste {
        display: flex;
        justify-content: space-around;
        align-items: center;
        padding: 4rem 0;
    }

    .logos {
        width: max-content;
        display: flex;
        align-items: center;
    }
</style>
