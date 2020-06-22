<template>
  <v-layout style="background-color:#222" d-flex justify-space-between align-center class="px-5">
    <nuxt-link to="/" class="brand">n|u</nuxt-link>
    <nav class="k-nav">
      <ul class="k-nav__menu d-flex flex-row justify-lg-space-between">
        <li
          :style="link.styleItem ? link.styleItem : ''"
          v-for="link in links"
          :key="link.name"
          class="k-nav__items"
          :class="link.class ? link.class : ''"
        >
          <nuxt-link
            :to="link.path"
            class="k-nav__link d-block px-6 py-4"
            :class="link.class ? link.class : ''"
          >
            <v-icon class="mr-1" color="white" dark>mdi-{{ link.icon }}</v-icon>
            {{ link.name }}
          </nuxt-link>
          <ul class="k-nav__menu--sub" v-if="link.submenu">
            <li class="k-nav__item--sub" v-for="sub in link.submenu" :key="sub">
              <nuxt-link class="k-nav__link--sub d-block px-6 py-4" :to="sub.path" >
                <v-icon class="mr-1" color="white" dark>mdi-{{ sub.icon }}</v-icon>
                {{ sub.name }}
              </nuxt-link>
            </li>
          </ul>
        </li>

        <li style="display: flex; align-items: center; cursor: pointer">
            <v-icon color="white" dark>mdi-invert-colors</v-icon>
        </li>          
      </ul>
    </nav>
  </v-layout>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  name: "Navbar",
  data() {
    return {
        methods: {
            invert(){
                // TODO implement dark mode toggle
            }
        },
      links: [
        {
          name: "Upcoming events",
          path: "/events",
          icon: "calendar-month",
          class: "",
        },
        { 
            name: "Archive", 
            path: "",
            icon: "archive",
            class: "k-nav__items--archive",
            styleItem: {
              position: "relative"
            },
            submenu: [
            { 
                name: "events", 
                path: "/events", 
                icon: "calendar-refresh" },
            { 
                name: "sessions", 
                path: "/sessions",
                icon: "" 
            },
          ]
        },
        { name: "Chapter", path: "" },
        { name: "Engage", path: "" },
        { name: "Social", path: "" },
        { name: "Blog", path: "" },
        { name: "login", path: "", class: "ml-8" },
        { name: "about", path: "" },
        { name: "support", path: "" }
      ]
    };
  }
});
</script>
<style lang="scss">
.brand {
  color: white !important;
  text-decoration: none;
  font-size: 2.5rem;
  font-weight: 400;
}
.k-nav {
  &__menu,
  &__menu--sub {
    list-style: none;
    padding: 0;
  }

  &__menu--sub {
    display: flex;
    display: none;
    flex-direction: column;
    position: absolute;
    padding-left: 0 !important;
    //   top: 0%;
    left: 0;
    right: 0;
    z-index: 9;
    text-align: left;
    background-color: transparentize($color: $color-tertiary-dark, $amount: .75);
  }

  &__items:hover &__menu--sub {
      display: flex;
  }

  &__link,
  &__link--sub {
    // color: white;
    text-decoration: none;
    cursor: pointer;
    transition: all 0.3s ease-in-out;

    &:hover,
    &:active {
      background-color: $color-tertiary-dark;
      color: white;
    }
  }
}
</style>