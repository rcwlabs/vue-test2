<template>
  <div id="app">
    <h1>{{ msg }}</h1>
    <User />
  </div>
</template>

<script>
import User from './components/User'

export default {
  data () {
    return {
      msg: 'This is MY Vue.js App'
    }
  },
  components: {
    User
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
