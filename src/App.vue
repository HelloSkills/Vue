<script>
export default {
  data() {
    return {
      users: [],
      error:'',
      userName: '',
      userPass: '',
      userEmail: ''
    }
  },
  methods: {
    sendData() {
      if (this.userName == '') {
        this.error = 'Введите имя';
        return;
      } else if (this.userPass == '') {
          this.error = 'Введите пароль'
          return
      } else if (this.userEmail == '') {
          this.error = 'Введите Email'
          return
        }

      this.error = '';

      this.users.push({
        name: this.userName,
        pass: this.userPass,
        email: this.userEmail
      })
    }

  }
}
</script>

<template>

  <input type="text" v-model="userName" placeholder="Имя">
  <input type="password" v-model="userPass" placeholder="Пароль">
  <input type="email" v-model="userEmail" placeholder="Почта">
  <p className="error">{{error}}</p>
  <button @click="sendData()">Отправить</button>
<div v-for="(el, index) in users" :key="index" class="user">
  <h3>{{el.name}}</h3>
  <p>{{el.email}} - <b>{{el.pass}}</b></p>
</div>

</template>



<style scoped>

input {
  display: flex;
  margin-top: 15px;
}

button {
  margin-top: 15px;
}

.user {
  width: 450px;
  margin-top: 20px;
  border: 1px solid silver;
  background: silver;
  color: black;
  padding: 10px;
  border-radius: 10px;
}

</style>
