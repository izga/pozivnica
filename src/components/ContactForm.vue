<template>
    <div class="container">
        <form @submit.prevent="sendEmail">
<!--          <label>Name</label>-->
<!--          <input -->
<!--            type="text" -->
<!--            v-model="name"-->
<!--            name="name"-->
<!--            placeholder="Your Name"-->
<!--          >-->
<!--          <label>Email</label>-->
<!--          <input -->
<!--            type="email" -->
<!--            v-model="email"-->
<!--            name="email"-->
<!--            placeholder="Your Email"-->
<!--            >-->
          <label>Upišite Vaše ime i imena bližnjih za koje znate da će doći</label>
          <textarea 
            name="message"
            v-model="message"
            cols="30" rows="5"
            placeholder="Prezime i imena...">
          </textarea>
          
          <input type="submit" value="Potvrdi">
        </form>
    </div>
</template>

<script>
import emailjs from 'emailjs-com';
import VueSimpleAlert from "vue-simple-alert";
import Vue from "vue"
Vue.use(VueSimpleAlert);

export default {
  name: 'ContactUs',
  data() {
    return {
      name: '',
      email: 'izgarevicdejana@gmail.com ',
      message: ''
    }
  },
  methods: {
    sendEmail(e) {
      try {
        emailjs.sendForm('service_s5jio7p', 'template_axj1x1e', e.target, 'iBbxI2b1oHt5unZ0A', {
          name: this.name,
          email: this.email,
          message: this.meessage
        });

      } catch (error) {
          console.log({error})
      }
      // Reset form field
      this.name = ''
      this.email = ''
      this.message = ''
      this.alert();
    },
    alert(){
      this.$alert("Uspešna potvrda");
    }
  }
}
</script>

<style scoped>
* {box-sizing: border-box;}

label {
  float: left;
  font-size: 2.2vmin ;
}
input[type=text], [type=email], textarea {
  width: 100%;
  padding: 12px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
  margin-top: 10px;
  margin-bottom: 16px;
  resize: vertical;
  font-size: 2vmin ;
}

input[type=submit] {
  background-color: #4CAF50;
  color: white;
  padding: 12px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  font-size: 2.2vmin;
}

input[type=submit]:hover {
  background-color: #b8c7b9;
}

.container {
  display: block;
  margin:auto;
  text-align: center;
  border-radius: 5px;
  background-color: #f2f2f2;
  padding: 2%;
}
</style>