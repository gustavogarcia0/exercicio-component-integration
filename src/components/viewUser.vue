<template>
  <div class="userMain">
    <p><strong>Nome:</strong> {{ userToShow.nome }}</p>
    <p><strong>Idade:</strong> {{ userToShow.idade }}</p>
  </div>
</template>

<script>
export default {
  name: "viewUser",

  props: {
    userToShow: {
      type: [Array],
      default() {
        return [];
      },
    },
  },
};
</script>

<style scoped>
.userMain {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 80%;
  padding: 15px 15px;
  margin: 0px 25px;
  border: 2px solid black;
}
</style>
