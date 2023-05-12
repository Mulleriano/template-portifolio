<script>
export default {
  data() {
    return {
      formData: {},
    };
  },
  methods: {
    enviaInput(event) {
      event.preventDefault();

      let dados = "";

      for (const chave of Object.keys(this.formData)) {
        dados += `${chave}: ${this.formData[chave]}, `;
      }

      alert (dados);
      this.formData = {};
    },
    recebeInput(event) {
      const nomeDoInput = event.target.name;
      const valorDoInput = event.target.value;

      this.formData[nomeDoInput] = valorDoInput;
    },
  },
};
</script>

<template>
  <form id="form" autocomplete="off" action="" @submit="enviaInput">
    <input
      class="input"
      type="text"
      name="Nome"
      placeholder="Name"
      :value="formData.Nome"
      @keyup="recebeInput"
    />

    <input
      class="input"
      type="email"
      name="Email"
      placeholder="Email"
      :value="formData.Email"
      @keyup="recebeInput"
    />

    <textarea
      class="input"
      name="Mensagem"
      placeholder="Message"
      :value="formData.Mensagem"
      @keyup="recebeInput"
      cols="30"
      rows="10"
    ></textarea>

    <button class="submit bold" type="submit">Submit</button>
  </form>
</template>

<style scoped>

.input {
  display: flex;
  flex-direction: column;
  padding: 2rem 1rem;
  width: 35vw;
  margin-bottom: 1rem;
  border: 0;
  background-color: #F3F3F3;
  color: #2D2D2D;
}

.submit {
  margin-top: 1rem;
  padding: 1.5rem 5rem;
  text-decoration: underline;
  font-size: 1.2rem;
  color: white;
  background-color: #2D2D2D;
  border: none;
  cursor: pointer;
  transition: all ease 0.3s;
}

.submit:hover {
  opacity: 0.8;
}

@media screen and (max-width:600px) {
  
  form {
    margin-top: 8vh;
  }

  .input {
    width: 100%;
  }
}
</style> 
