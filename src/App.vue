<template>
  <div id="app" role="main">
    <Header />
    <Countries :info='info' />
  </div>
</template>

<script>
import Header from './components/Header'
import Countries from './components/Countries'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    Header,
    Countries
  },
  data() {
    return {
      info: [],
    }
  },
  mounted() {
    axios
      .get('https://api.covid19api.com/summary')
      .then(response => (this.info = response.data.Countries))
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: #2c3e50;
  text-align: center;
}
</style>
