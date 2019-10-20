<template>
  <div id="app">
    <nav class="nav">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
    </nav>

    <router-view />
  </div>
</template>

<script>
export default {
  name: 'app',
  components: {
  }
}
</script>

<style>
  body {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    display: grid;
    grid-template-rows: auto;
    justify-items: center;
    align-items: center;
    background-color: #f8f8f8;
  }
  body, html {
    margin: 0;
    height: 100%;
  }
  #app {
    width: 50%;
  }
  .nav {
    margin-bottom: 20px;
  }
  .nav a {
    text-decoration: none;
    display: inline-block;
    padding: 15px 20px;
    background: #ddd;
    margin-right: 20px;
    color: black;
    border-radius: 5px;
  }


</style>
