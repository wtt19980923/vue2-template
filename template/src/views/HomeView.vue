<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <h1>欢迎使用 Vue2 模板</h1>
    <p>当前计数: {{ count }}</p>
    <button @click="increment">增加</button>
    <button @click="incrementAsync">异步增加</button>
  </div>
</template>

<script>
import { mapState, mapMutations, mapActions } from 'vuex'

export default {
  name: 'HomeView',
  computed: {
    ...mapState(['count'])
  },
  methods: {
    ...mapMutations(['increment']),
    ...mapActions(['incrementAsync'])
  }
}
</script>

<style scoped>
.home {
  margin-top: 40px;
}

button {
  margin: 0 10px;
  padding: 10px 20px;
  background-color: #42b983;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #3aa876;
}
</style> 