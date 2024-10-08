<template>
  <div class="userDataMain">
    <table border="1" width="500">
      <thead>
        <tr>
          <th>Nome</th>
          <th>Idade</th>
        </tr>
        <tr v-for="item in objUserData" :key="item.nome">
          <th @click="$emit('selectedUser', item)">{{ item.nome }}</th>
          <th @click="$emit('selectedUser', item)">{{ item.idade }}</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "usersData",

  props: {
    objUserData: {
      type: [Array],
      default() {
        return [];
      },
    },
  },
};
</script>

<style scoped>
.userDataMain {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 80%;
  padding: 15px 15px;
  margin: 0px 25px;
}
</style>
