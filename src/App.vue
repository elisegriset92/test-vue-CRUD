<template>
  <div id="app">
    <router-view/>
           <footer> Made with 🍭 by Elise Griset</footer>

  </div>
</template>

<script>
export default {
  name: 'Teste Vue Posts',
};
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
footer {
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  background-color: #e9bf00;
  color: white;
  text-align: center;
}
</style>
