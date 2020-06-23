<template>
  <v-app dark>
    <Navbar />

    <v-content>
        <nuxt />
    </v-content>

    <!-- <span>&copy; {{ new Date().getFullYear() }}</span> -->
    <Footer />
  </v-app>
</template>

<script>
import Footer from "../components/footer";
import Navbar from "../components/navbar";
export default {
  components: {
    Footer,
    Navbar
  },
  data() {
    return {};
  }
};
</script>
