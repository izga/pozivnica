<template>
  <div id="app">
    <div id="pozivnica-container">
      <img alt="Pozivnica" src="./assets/pozivnica.jpeg" loading="lazy">
    </div>
    <br>
    <p>Molimo potvrdite Vaš dolazak najkasnije do 15.07.2022. godine putem sledeće forme: </p>
    <div id="forma">
      <contact-form/>
    </div>
    <br>
    <div id="mobile-form">
      <p>Vaš dolazak možete potvrditi i putem mobilnog telefona:</p>
      <p>Mladoženja: <a href="tel:+381607606515">+381607606515</a></p>
      <p>Mlada: <a href="tel:+381654501379">+381654501379</a></p>
    </div>
    <br>
    <div id="map-container">
      <a href="https://goo.gl/maps/zNuXFVtMzmqnqmhQA" target="_blank"><img alt="Pozivnica" src="./assets/maps.png"></a>
      <h4>Kliknite mapu za precizniju lokaciju.</h4>
    </div>
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
  margin-bottom: 40px;
}

#mobile-form {
  /*all is good*/
}

p {
  font-size: 2.8vmin;
}

#forma {
  max-width: 1800px;
  display: inline-block;
  margin-bottom: 20px;
}

#pozivnica-container {
  max-width: 95.5vmin;
  display: inline-block;
  margin-bottom: 10px;
}

#map-container {
  max-width: 95.5vmin;
  display: inline-block;
}

a, img {
  width: 100%;
  width: -moz-available; /* WebKit-based browsers will ignore this. */
  width: -webkit-fill-available; /* Mozilla-based browsers will ignore this. */
  width: fill-available;
}
@media only screen and (max-width: 480px) {
img{
  width: 360px;
}
}

h4 {
font-size: 1.8vmin;
}
</style>
