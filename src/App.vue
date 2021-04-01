<template>
  <img alt="Vue logo" src="./assets/logo1.png">
  <!-- <HelloWorld msg="Welcome to Your Vue.js App by uto"/> -->
  <Title text="Tu Banco Del Despertar 3.0" />
  <Cuenta/>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Title from './components/Title';
import Cuenta from './components/Cuenta';
// import Title from './components/Title.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
    Title,
    Cuenta
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
img{
  width: 300px;
  }
</style>
