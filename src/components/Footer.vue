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
              <li><NuxtLink :to="localePath('/')">{{ $t('footer.bottom.left.links.home') }}</NuxtLink></li>
              <li><NuxtLink :to="localePath('privacypolicy')">{{ $t('footer.bottom.left.links.privacypolicy') }}</NuxtLink></li>
              <li><NuxtLink :to="localePath('impressum')">{{ $t('footer.bottom.left.links.impressum') }}</NuxtLink></li>
            </div>
            <div class="right">
              <li v-if="isHomePage"><NuxtLink to="#About">{{ $t('footer.bottom.right.links.about') }}</NuxtLink></li>
              <li v-if="isHomePage"><NuxtLink to="#Contact">{{ $t('footer.bottom.right.links.contact') }}</NuxtLink></li>
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
<script setup>
import { useLocalePath } from '#imports'
const localePath = useLocalePath()
const route = useRoute()
const isHomePage = computed(() => {
  // dla stron z prefiksem języka, np. /en lub /de
  const path = route.path.replace(/^\/(en|de)/, '')
  return path === '/' || path === ''
})
</script>