<script>
import client1 from "../assets/clients/client1.png";
import client2 from "../assets/clients/client2.png";
import client3 from "../assets/clients/client3.png";

import Clients from "./Clients.vue";

export default {
  components: {
    Clients,
  },
  data() {
    return {
      clients: [
        {
          text: "This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com",
          userImg: client1,
          userName: "Gemma Nolen,",
          userCompany: "Google",
        },
        {
          text: "This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com",
          userImg: client2,
          userName: "Gemma Nolen,",
          userCompany: "Google",
        },
        {
          text: "This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com",
          userImg: client3,
          userName: "Gemma Nolen,",
          userCompany: "Google",
        },
      ],
    };
  },
};
</script>
<template>
  <div class="container">
    <h2>Clients</h2>
    <div class="avaliacao">
      <div v-for="client in clients">
        <Clients
          :text="client.text"
          :userImg="client.userImg"
          :userName="client.userName"
          :userCompany="client.userCompany"
        />
      </div>
    </div>
  </div>
</template>

<style scoped>
.avaliacao {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  flex-wrap: wrap;
}

h2 {
  text-align: center;
  font-size: 2rem;
  padding-bottom: 3rem;
}

@media screen and (max-width: 600px) {
  .avaliacao {
    flex-direction: column;

  }
}
</style>
