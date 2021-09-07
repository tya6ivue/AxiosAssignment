<template>
  <div id="app">
    <!-- <HomePage /> -->
    <PostMethods />
  </div>
</template>

<script>
// import HomePage from './components/HomePage.vue'
import PostMethods from './components/PostMethods.vue'

export default {
  name: 'App',
  components: {
    // HomePage,
    PostMethods
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
