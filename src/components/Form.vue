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
  <form action="" @submit="enviaInput">
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

    <button type="submit">Submit</button>
  </form>
</template>
