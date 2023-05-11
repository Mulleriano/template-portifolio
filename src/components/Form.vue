<script>
export default {
  data() {
    return {
      Nome: "",
      Email: "",
      Mensagem: "",
    };
  },
  methods: {
    enviaInput(event) {
      event.preventDefault();

      console.log({
        Nome: this.Nome,
        Email: this.Email,
        Mensaem: this.Mensagem
      })
    },
    recebeInput(event) {
      const nomeDoInput = event.target.name;
      const valorDoInput = event.target.value;

      this[nomeDoInput] = valorDoInput;
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
      :value="name"
      @keyup="recebeInput"
    />

    <input
    class="input" 
    type="email"
    name="email"
    placeholder="Email"
    :value="Email"
    @keyup="recebeInput"
    />

    <textarea
    class="input"
    name="Mensagem"
    placeholder="Message"
    :value="Mensagem"
    @keyup="recebeInput"
    cols="30"
    rows="10"
    ></textarea>

    <button type="submit">Submit</button>
  </form>
</template>
