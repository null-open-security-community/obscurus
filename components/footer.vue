<template>
        <footer class="footer">
      <div class="footer__logo-box">
        <picture  class="footer__logo">
            <img src="../assets/images/null.svg" alt="">
          <!-- <source media="(max-width: 37.5em)" srcset="img/logo-green-small-1x.png 1x, img/logo-green-small-2x.png 2x"> -->
          <!-- <img srcset="img/logo-green-1x.png 1x, img/logo-green-2x.png 2x" src="img/logo-green-1x.png" alt="Natours"/> -->
        </picture>
      </div>
      <div class="row">
        <div class="col-1-of-2">
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
        </div>
        <div class="col-1-of-2">
          <p class="footer__copyright">
            null - The Open Security Community &copy; {{ new Date().getFullYear() }}
            <br/> 
            null is India's largest open security community. Registered as a non-profit society in 2010.
          </p>
        </div>
      </div>
    </footer>
</template>
