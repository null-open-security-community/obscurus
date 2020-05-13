<template>
  <div>
    <v-container fill-height fluid>
        <v-col justify="center"  cols="12">
          
          <nullIntro></nullIntro>
          <!-- Logo component goes here  -->
        </v-col>
     </v-container>
  </div>
</template>

<script>
import nullIntro from "~/components/nullIntro.vue";

export default {
  components: {
    nullIntro: nullIntro
  }
};
</script>
