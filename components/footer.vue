<template>
<v-container fluid>
  <footer class="footer">
    <div class="footer__logo-box">
      <picture class="footer__logo">
        <img src="../assets/images/null.svg" alt />
        <!-- <source media="(max-width: 37.5em)" srcset="img/logo-green-small-1x.png 1x, img/logo-green-small-2x.png 2x"> -->
        <!-- <img srcset="img/logo-green-1x.png 1x, img/logo-green-2x.png 2x" src="img/logo-green-1x.png" alt="Natours"/> -->
      </picture>
    </div>
    <v-row justify="center">
      <v-col cols="12" xs="3" sm="9" md="6" lg="6" xl="6" class="mb-sm-6">
        <v-row justify="center">
          <div class="footer__navigation">
            <ul class="footer__list">
              <li class="footer__item">
                <nuxt-link to="#" class="footer__link">Company</nuxt-link>
              </li>
              <li class="footer__item">
                <nuxt-link to="#" class="footer__link">Contact us</nuxt-link>
              </li>
              <li class="footer__item">
                <nuxt-link to="#" class="footer__link">Careers</nuxt-link>
              </li>
              <li class="footer__item">
                <nuxt-link to="#" class="footer__link">Privacy policy</nuxt-link>
              </li>
              <li class="footer__item">
                <nuxt-link to="#" class="footer__link">Terms</nuxt-link>
              </li>
            </ul>
          </div>
        </v-row>
      </v-col>
      <v-col cols="12" xs="3" sm="9" md="6" lg="6" xl="6">
        <v-row justify="center">
          <p class="footer__copyright">
            null - The Open Security Community &copy; {{ new Date().getFullYear() }}
            <br />null is India's largest open security community. Registered as a non-profit society in 2010.
          </p>
        </v-row>
      </v-col>
    </v-row>
  </footer>
  </v-container>
</template>
