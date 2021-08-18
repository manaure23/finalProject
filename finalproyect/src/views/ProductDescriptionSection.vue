<template>
  <section id="productDescription">
    <Header/>
    <ProductDescriptionPage/>
    <Footer/>
  </section>
</template>

<script>
import Header from '@/components/Header.vue'
import ProductDescriptionPage from '@/components/ProductDescriptionPage.vue'
import Footer from '@/components/Footer.vue'
export default {
  name: 'ProductDescriptionSection',
  components: {
    Header,
    ProductDescriptionPage,
    Footer,
  }
}
</script>

<style>

</style>