<template>
  <v-app dark>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>

      <!-- <span>&copy; {{ new Date().getFullYear() }}</span> -->
      <Footer />
  </v-app>
</template>

<script>
import Footer from "../components/footer"
export default {
  components:{
    Footer
  },
  data() {
    return {
    };
  }
};
</script>
