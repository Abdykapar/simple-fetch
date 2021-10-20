<template>
  <div id="app">
    <HelloWorld :todos="todos" />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
  },
  data() {
    return {
      todos: []
    }
  },
  mounted () {
    this.fetchData()
  },
  methods: {
    fetchData () {
      fetch('https://jsonplaceholder.typicode.com/todos')
      .then(res => res.json())
      .then(json => this.todos = json)
    }
  }
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
