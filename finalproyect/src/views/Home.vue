<template>
  <section id="home">
    <Header/>
    <Homepage/>
    <Footer/>
  </section>
</template>

<script>
// @ is an alias to /src
import Homepage from '@/components/Homepage.vue'
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'Home',
  components: {
    Homepage,
    Header,
    Footer
  }
}
</script>
