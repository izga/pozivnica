<template>
  <div id="app">
    <img alt="Pozivnica" src="./assets/pozivnica.jpeg">
    <p>Molimo potvrdite Vaš dolazak najkasnije do 15.07.2022. godine putem sledeće forme: </p>
    <contact-form />
  </div>
</template>

<script>
import ContactForm from './components/ContactForm.vue'

export default {
  name: 'App',
  components: {
    ContactForm
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

p {
  font-size: 28px;
}

img {
  width: 700px;
  padding-bottom: 60px;
}
</style>
