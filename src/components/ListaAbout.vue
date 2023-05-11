<script>
import about1 from "../assets/about/about1.svg";
import about2 from "../assets/about/about2.svg";
import about3 from "../assets/about/about3.svg";

import About from "./About.vue";

export default {
  components: {
    About,
  },
  data() {
    return {
      abouts: [
        {
          src: about1,
          titulo: "Product design",
          text: "This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com",
        },
        {
          src: about2,
          titulo: "Art direction",
          text: "This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com",
        },
        {
          src: about3,
          titulo: "Visual design",
          text: "This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com",
        },
      ],
    };
  },
};
</script>
<template>
  <div class="container">
    <div v-for="about in abouts">
      <About :src="about.src" :titulo="about.titulo" :text="about.text" />
    </div>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  text-align: center;
}

@media screen and (max-width: 600px){
  .container {
    flex-direction: column;
    justify-content: center;
  }
}
</style>
