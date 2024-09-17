<script>
export default {
  data() {
    return {
    userName: '',
      userPass: '',
      userEmail: ''
    }
  },
  methods: {
    insertData(val) {
    this.userName = val
    }
  }
}
</script>

<template>

  <input type="text" v-model="userName" placeholder="Имя">
  <input type="password" v-model="userPass" placeholder="Пароль">
  <input type="email" v-model="userEmail" placeholder="Почта">
  <p>{{userName}}</p>
  <p>{{userPass}}</p>
  <p>{{userEmail}}</p>

</template>


<style scoped>


</style>
