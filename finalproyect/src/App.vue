<template>
  <div>
    <Header msg="Welcome to Your Vue.js App"/>
    <Homepage/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Homepage from './components/Homepage.vue'
import Footer from './components/Footer.vue'
export default {
  name: 'App',
  components: {
    Header,
    Homepage,
    Footer
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
}
</style>
