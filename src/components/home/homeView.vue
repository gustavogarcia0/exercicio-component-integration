<template>
  <div class="homeMain">
    <usersData :objUserData="objUserData" @selectedUser="selectedUser = $event" />
    <viewUser :userToShow="selectedUser" />
  </div>
</template>

<script>
import usersData from "../usersData.vue";
import viewUser from "../viewUser.vue";

export default {
  name: "homeView",
  components: {
    usersData,
    viewUser,
  },

  data() {
    return {
      objUserData: [
        {
          nome: "Ana",
          idade: "22 anos",
        },
        {
          nome: "Marcos",
          idade: "27 anos",
        },
        {
          nome: "Rodrigo",
          idade: "33 anos",
        },
      ],
      selectedUser: {},
    };
  },

  watch: {
    selectedUser: {
      handler(newValue) {
        console.log(newValue.nome);
      },
      deep: true,
    },
  },
};
</script>

<style scoped>
.homeMain {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
</style>
