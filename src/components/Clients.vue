<script>
export default {
  props: {
    text: String,
    userImg: String,
    userName: String,
    userCompany: String,
  },
};
</script>

<template>
  <div class="container">
    <div class="avaliacao">
      <p class="text bold">{{ text }}</p>

      <div class="user">
        <img :src="userImg" alt="Client" />
        <div class="userInfos">
          <img src="../assets/clients/stars.svg" alt="estrelas" />
          <p>
            {{ userName }} <br />
            {{ userCompany }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.avaliacao {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: 1.7rem;
  background-color: #f3f3f3;
  width: 300px;
  height: 50vh;
  margin: 30px 15px;
}

.text {
  font-size: 1.3rem;
  line-height: 1.9rem;
}

.user {
  display: flex;
}

.user > img {
  height: min-content;
  margin-right: 1rem;
}

@media screen and (max-width: 600px) {
  .avaliacao {
    width: auto;
    margin: 6vh 1.5vw;
  }
}
</style>
