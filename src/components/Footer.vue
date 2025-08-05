<template>
  <footer class="footer">
    <div class="footer__content">
      <div class="footer__top">
        <div class="footer__top--support">
          <div class="icon">
            <NuxtImg src="/images/footer/heart.svg"/>
          </div>
          <div class="text">
            support us
            <span>lorem ipsum</span>
          </div>
        </div>
        <div class="footer__top--vl"></div>
        <div class="footer__top--iban">
          <div class="number">
            IBAN 00 0100 0000 1234 5678 9100
          </div>
          <div class="text">
            lorem ipsum dolor sit amet
          </div>
          <div class="paymentIcons">
            <NuxtImg src="/images/footer/paypal.svg"/>
            <NuxtImg src="/images/footer/visa.svg"/>
            <NuxtImg src="/images/footer/card.svg"/>
          </div>
        </div>
      </div>
      <div class="footer__bottom">
          <div class="footer__bottom--top">
            <div class="left">
              <h1>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ullam</h1>
              <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ullam ratione non nostrum.</p>
            </div>
            <div class="right">
              <li><NuxtLink to="#">About</NuxtLink></li>
              <li><NuxtLink to="#">About</NuxtLink></li>
              <li><NuxtLink to="#">About</NuxtLink></li>
              <li><NuxtLink to="#">About</NuxtLink></li>
            </div>
          </div>
          <hr>
          <div class="footer__bottom--bot">
            <p>Lorem, ipsum dolor.</p>
          </div>
        </div>
      </div>
  </footer>
</template>