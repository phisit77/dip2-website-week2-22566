<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <AboutPage />
  <ContactPage />
  <h3>The Progressive JavaScript Framework</h3>
  <h3>{{ msg }}</h3>
  <p>Using text interpolation: {{ buttonHTML }}</p>
  <p>Using v-html directive: <span v-html="buttonHTML"></span></p>
  <p v-bind:style="color">TEST</p>
  <a :href="web">Google</a>
  {{ 2*4 }}
  <h2 :style="`color:${savings >= 200 ? 'green': 'red'}`">${{ savings }}</h2>
  <h2 :class=" savings >= 200 ? 'bottom':'background' ">${{ savings }}</h2>
</template>

<style>
  .bottom{
    color: red;
  }
  .background{
    color: green;
  }
</style>

<script>
import AboutPage from './components/AboutPage.vue';
import ContactPage from './components/ContactPage.vue'
const buttonHTML = "<button>Click Me</button>"
const color = "color:white;background-color:blueviolet;"
const web = "https://www.google.com" 
const savings = 150
export default {
  name: "App",
  components: {
    AboutPage,
    ContactPage,
  },
  data() {
    return {
      msg: "Hello",
      buttonHTML,
      color,
      web,
      savings,
    }
  }
};
</script>

