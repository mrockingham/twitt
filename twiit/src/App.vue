<template>
  <div id="app">
<UProfile />
  </div>
</template>

<script>
import UProfile from "./components/UProfile"

export default {
  name: 'App',
  components: {
    UProfile
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  
  color: #2c3e50;
  margin-top: 60px;
}
</style>
