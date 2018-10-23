<template>
  <div id="app">
      <calculadora></calculadora>
  </div>
</template>

<script>
import calculadora from "./components/calculadora.vue";

export default {
  name: "app",
  components: {
    calculadora
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  width: 100%; 
  height: 100%;
}
</style>
