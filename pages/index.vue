<template>
  <v-container fluid>
    <v-row justify="space-around" class="bg">
      <v-col justify="center">
        <nullIntro></nullIntro>
      </v-col>
    </v-row>

    <!-- cards -->

    <v-row justify="space-around">
      <v-col cols="12" md="3">
        <v-card shaped dark>
          <v-card-title class="display-1">Subscribe to group</v-card-title>
          <v-card-text style="font-size: 1.5rem; line-height: 1">Join the mailing list to keep yourself updated about our activities & events. Join it for deep technical discussions revolving around computer security & nothing else. Some of the best security professionals answer queries, discuss new findings and more, all in the mailing list.</v-card-text>
          <v-card-actions>
            <v-btn text color="deep-purple accent-4">Subscribe to group</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
      <v-col
        cols="12"
        md="3"
      >Join the mailing list to keep yourself updated about our activities & events. Join it for deep technical discussions revolving around computer security & nothing else. Some of the best security professionals answer queries, discuss new findings and more, all in the mailing list.</v-col>
      <v-col
        cols="12"
        md="3"
      >Join the mailing list to keep yourself updated about our activities & events. Join it for deep technical discussions revolving around computer security & nothing else. Some of the best security professionals answer queries, discuss new findings and more, all in the mailing list.</v-col>
    </v-row>
  </v-container>
</template>

<script>
import nullIntro from "~/components/nullIntro.vue";
export default {
  components: {
    nullIntro: nullIntro
  }
};
</script>

<style lang="scss">
.bg {
  background-image: linear-gradient(
      to right,
      rgba(cyan, 0.9),
      rgba(purple, 0.3)
    ),
    url("../assets/images/background.jpg");
  background-size: cover;
  background-position: center;
}
</style>
