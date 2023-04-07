<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <Jobs msg="Nomad Job Runner" />
  <GetJobs />
  <GetCompanies />
</template>

<script>
import Jobs from './components/Jobs.vue'
import GetJobs from './components/GetJobs.vue'
import GetCompanies from './components/GetCompanies.vue';

export default {
  name: 'App',
  components: {
    Jobs,
    GetJobs,
    GetCompanies
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
