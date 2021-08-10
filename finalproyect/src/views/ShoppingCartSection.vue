<template>
  <div>
    <Header/>
    <ShoppingCartPage/>
    <Footer/>
  </div>

</template>

<script>
import Header from '@/components/Header.vue'
import ShoppingCartPage from '@/components/ShoppingCartPage.vue'
import Footer from '@/components/Footer.vue'
export default {
  name: 'ShopingCartSection',
  components: {
    Header,
    ShoppingCartPage,
    Footer,
  }
}
</script>

<style>

</style>
