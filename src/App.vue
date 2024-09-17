<script>
export default {
data() {
  return {
    info: 'Title',
    someInfo: 'Anons of message'
  }
}
}
</script>

<template>
<h3>{{info}}</h3>
  <p>{{someInfo}}</p>

  <button type="button" @click="this.info = 'Some New'" class="btn">Отправить</button>
</template>


<style scoped>

h3 {
  display:flex;
  text-align: center;
  color: green;
  justify-content: center;
  font-weight: lighter;
}

p {
  color: rgb(203, 31, 31);
  display:flex;
  text-align: center;
  justify-content: center;
}

.btn {
  display:flex;
  text-align: center;
  justify-content: center;
  width: 100%;
}

</style>
