<template>
  <div id="app">
    <h1>Vue-Piano <small>(Actually more like Vue-Synth)</small></h1>
    <p>Simple Piano example using <a href="https://github.com/vuejs/vue" target="_blank">Vue.js</a> and <a href="https://github.com/Tonejs/Tone.js" target="_blank">Tone.js</a></p>
    <p><em>Is still work in progress...</em></p>
    <piano></piano>
    <p>Made by <a href="https://twitter.com/juanda95" target="_blank">@juanda95</a></p>
    <p>You can find the code at <a href="https://github.com/juanda95/vue-piano">vue-piano</a></p>
  </div>
</template>

<script>
import Piano from './components/Piano'

export default {
  name: 'app',
  components: {
    Piano
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
  margin: 0 auto;
  margin-top: 60px;
}

small {
  font-size: 11px;
}
</style>
