<template>
  <v-layout d-flex justify-space-between align-center class="px-5 sticky">
    <nuxt-link to="/" class="brand">n|u</nuxt-link>
    <nav class="k-nav">
      <ul class="k-nav__menu d-flex flex-row justify-lg-space-between">
        <li
          :style="link.styleItem ? link.styleItem : ''"
          v-for="(link, index) in links"
          :key="index"
          class="k-nav__items"
          :class="link.class ? link.class : ''"
        >
          <nuxt-link
            :to="link.path"
            class="k-nav__link d-flex align-center px-4 py-4"
            :class="link.class ? link.class : ''"
          >
            <v-icon class="mr-2" color="black" dark>mdi-{{ link.icon }}</v-icon>
            {{ link.name }}
          </nuxt-link>
          <ul class="k-nav__menu--sub" v-if="link.submenu">
            <li class="k-nav__item--sub" v-for="(sub, index) in link.submenu" :key="index">
              <nuxt-link class="k-nav__link--sub d-flex align-center px-4 py-4" :to="sub.path">
                <v-icon class="mr-2" color="black" dark>mdi-{{ sub.icon }}</v-icon>
                {{ sub.name }}
              </nuxt-link>
            </li>
          </ul>
        </li>
        <!-- TODO implement dark mode toggle -->
        <!-- <li style="display: flex; align-items: center; cursor: pointer">
            <v-icon color="white" dark class="px-4">mdi-invert-colors</v-icon>
        </li>-->
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
        invert() {
          // TODO implement dark mode toggle
        }
      },
      links: [
        {
          name: "Upcoming events",
          path: "/events",
          icon: "calendar-month",
          class: ""
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
              icon: "calendar-refresh"
            },
            {
              name: "sessions",
              path: "/sessions",
              icon: "iframe"
            }
          ]
        },
        {
          name: "Chapter",
          path: "",
          icon: "account-multiple-plus"
        },

        {
          name: "Engage",
          path: "",
          icon: "account-group"
        },
        {
          name: "Blog",
          path: "",
          icon: "rss-box",
          // styleItem: {
          //   position: "relative"
          // },
          // submenu: [
          //   {
          //     name: "events",
          //     path: "/events",
          //     icon: "calendar-refresh"
          //   },
          //   {
          //     name: "sessions",
          //     path: "/sessions",
          //     icon: ""
          //   }
          // ]
        },

        {
          name: "login",
          path: "",
          icon: "account",
          class: "ml-4"
        },

        {
          name: "about",
          path: "",
          icon: "book-open mdi-rotate-315"
        }
      ]
    };
  }
});
</script>
<style lang="scss">
.sticky {
  position: sticky;
  top: 0;
  background-color: $color-secondary;
  z-index: 1;
  box-shadow: 0px 2px 5px black;
}
.brand {
  color: black !important;
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
    // right: 0; width becomes 100% of parent li
    z-index: 9;
    text-align: left;
    background-color: transparentize(
      $color: $color-tertiary-dark,
      $amount: 0.75
    );
    box-shadow: 0px 2px 5px black;
  }

  &__items--sub {
    display: flex;
    align-items: center;
  }

  &__items:hover &__menu--sub {
    display: flex;
    background-color: $color-secondary-dark;
  }

  &__link,
  &__link--sub {
    color: black !important;
    text-decoration: none;
    cursor: pointer;
    transition: all 0.3s ease-in;

    &:hover,
    &:active {
      background-color: $color-tertiary-dark;
      color: white;
    }
  }

  &__link--sub {
    color: white !important;
  }
}
</style>