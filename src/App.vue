<template>
  <div id="app">
  <TweetCollection/>
  </div>
</template>

<script>
import TweetCollection from './components/TweetCollection.vue'

export default {
  name: 'App',
  components: {
    TweetCollection
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
