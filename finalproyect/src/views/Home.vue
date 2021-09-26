<template>
  <Header />
  <Homepage />
  <Footer />
</template>

<script>
// @ is an alias to /src
import Homepage from "@/components/Homepage.vue";
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "Home",
  components: {
    Homepage,
    Header,
    Footer,
  },
};
</script>
