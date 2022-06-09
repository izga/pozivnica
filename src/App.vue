<template>
  <div id="app">
    <img alt="Pozivnica" src="./assets/pozivnica.jpeg">
    <p>Molimo potvrdite Vaš dolazak najkasnije do 15.07.2022. godine putem sledeće forme: </p>
    <contact-form />
    <br>
    <div id="mobile-form">
    <p>Vaš dolazak možete potvrditi i putem mobilnog telefona:</p>
    <p>Mladoženja: +381607606515</p>
    <p>Mlada: +381654501379</p>
    </div>
    <br>
    <a href="https://goo.gl/maps/zNuXFVtMzmqnqmhQA" target="_blank"><img alt="Pozivnica" src="./assets/maps.png"></a>
    <h4>Kliknite mapu za precizniju lokaciju.</h4>
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

#mobile-form {

}

p {
  font-size: 28px;
}

img {
  width: 700px;
  padding-bottom: 60px;
}
</style>
