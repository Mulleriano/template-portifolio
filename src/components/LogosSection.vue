<script>
import adidas from "../assets/logos/adidas.png";
import apple from "../assets/logos/apple.png";
import google from "../assets/logos/google.png";
import intercom from "../assets/logos/intercom.png";
import nike from "../assets/logos/nike.png";
import samsung from "../assets/logos/samsung.png";

export default {
  data() {
    return {
      logos: [
        {
          src: google,
          alt: "Google",
        },
        {
          src: nike,
          alt: "Nike",
        },
        {
          src: samsung,
          alt: "Samsung",
        },
        {
          src: apple,
          alt: "Apple",
        },

        {
          src: intercom,
          alt: "Intercom",
        },
        {
          src: adidas,
          alt: "Adidas",
        },
      ],
    };
  },
};
</script>

<template>
  <div class="container">
    <div class="logos" v-for="logo in logos">
      <img :src="logo.src" :alt="logo.alt" />
    </div>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logos {
  width: max-content;
  display: flex;
  align-items: center;
}
</style>
