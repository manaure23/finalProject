<template>
  <div>
    <Header/>
    <FavoritesPage/>
    <Footer/>
  </div>

</template>

<script>
import Header from '@/components/Header.vue'
import FavoritesPage from '@/components/FavoritesPage.vue'
import Footer from '@/components/Footer.vue'
export default {
  name: 'FavoritesSection',
  components: {
    Header,
    FavoritesPage,
    Footer,
  }
}
</script>

<style>

</style>