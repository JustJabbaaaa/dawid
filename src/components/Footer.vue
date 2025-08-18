<template>
  <footer id="Footer" class="footer">
    <div class="footer__content">
      <div class="footer__top">
        <div class="footer__top--support">
          <div class="icon">
            <NuxtImg src="/images/footer/heart.svg"/>
          </div>
          <div class="text">
            {{ $t('footer.top.support.supportus') }}
          </div>
        </div>
        <div class="footer__top--vl"></div>
        <div class="footer__top--iban">
          <div class="thanksForSupport">
            {{ $t('footer.top.thanksForSupport') }}
          </div>
          <div class="number">
            IBAN 00 0100 0000 1234 5678 9100
          </div>
          <div class="text">
            <!-- {{$t('footer.top.ibanText')}} -->
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
              <!-- <h1>{{ $t('footer.bottom.left.text1') }}</h1> -->
              <!-- <p>{{ $t('footer.bottom.left.text2') }}</p> -->
            </div>
            <div class="right">
              <li><NuxtLink to="#About">{{ $t('footer.bottom.right.links.about') }}</NuxtLink></li>
              <li><NuxtLink to="#Contact">{{ $t('footer.bottom.right.links.contact') }}</NuxtLink></li>
              <li><NuxtLink to="#Navbar">{{ $t('footer.bottom.right.links.toTop') }}</NuxtLink></li>
            </div>
          </div>
          <hr>
          <div class="footer__bottom--bot">
            <!-- <p>{{$t('footer.bottom.right.text')}}</p> -->
          </div>
        </div>
      </div>
  </footer>
</template>