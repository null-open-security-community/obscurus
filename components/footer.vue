<template>
        <footer class="footer">
      <div class="footer__logo-box">
        <picture  class="footer__logo">
            <img src="../assets/images/null.png" alt="">
          <!-- <source media="(max-width: 37.5em)" srcset="img/logo-green-small-1x.png 1x, img/logo-green-small-2x.png 2x"> -->
          <!-- <img srcset="img/logo-green-1x.png 1x, img/logo-green-2x.png 2x" src="img/logo-green-1x.png" alt="Natours"/> -->
        </picture>
      </div>
      <div class="row">
        <div class="col-1-of-2">
          <div class="footer__navigation">
            <ul class="footer__list">
              <li class="footer__item">
                <a href="#" class="footer__link">Company</a>
              </li>
              <li class="footer__item">
                <a href="#" class="footer__link">Contact us</a>
              </li>
              <li class="footer__item">
                <a href="#" class="footer__link">Careers</a>
              </li>
              <li class="footer__item">
                <a href="#" class="footer__link">Privacy policy</a>
              </li>
              <li class="footer__item">
                <a href="#" class="footer__link">Terms</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="col-1-of-2">
          <p class="footer__copyright">
            null - The Open Security Community &copy; {{ new Date().getFullYear() }}
          </p>
        </div>
      </div>
    </footer>
</template>
