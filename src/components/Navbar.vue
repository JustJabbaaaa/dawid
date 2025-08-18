<template>
  <div id="Navbar" :class="{'subpage': !isHomePage }">
    <div class="nav">
      <NuxtLink :to="localePath('/')" class="nav__brand" aria-label="Go to homepage">
        {{ $t('navbar.logo.yourCandidate') }}<br/>{{ $t('navbar.logo.mayor') }}<br class="linebreak" v-if="$i18n.locale === 'de'" /> <NuxtImg src="/images/vision/herb.webp"/><span>Oranienburg</span></NuxtLink>
      <div class="nav__buttons">
        <div class="nav__buttons--navMenu" v-if="isHomePage">
          <li class="nav__buttons--item"><NuxtLink to="#About" class="nav__buttons--btn">{{ $t('navbar.links.about') }}</NuxtLink></li>
          <li class="nav__buttons--item"><NuxtLink to="#Footer" class="nav__buttons--btn">{{ $t('navbar.links.support') }}</NuxtLink></li>
          <li class="nav__buttons--item"><NuxtLink to="#Contact" class="nav__buttons--btn">{{ $t('navbar.links.contact') }}</NuxtLink></li>
        </div>
        <div class="nav__buttons--navSocials">
          <div class="socials">
            <!-- <NuxtLink to=""><NuxtImg src="images/navbar/twitter.svg" alt="twitter" class="social"/></NuxtLink> -->
            <!-- <NuxtLink to=""><NuxtImg src="images/navbar/fb.svg" alt="facebook" class="social"/></NuxtLink> -->
            <NuxtLink to="https://www.instagram.com/heiko.zillmann.oranienburg?igsh=MWJwcGpkeTE0ZGp3Zg%3D%3D&utm_source=qr"><NuxtImg src="images/navbar/insta.svg" alt="instagram" class="social"/></NuxtLink>
            <NuxtLink to="https://whatsapp.com/channel/0029VbBH4U4HFxP30b6sO342"><NuxtImg src="images/navbar/whatsapp.svg" alt="whatsapp" class="social"/></NuxtLink>
          </div>
          <div class="langs">
            <NuxtLink class="lang"@click.prevent="setLocale('en')" :class="{ 'active': locale === 'en' }">EN</NuxtLink>
            <span>/</span>
            <NuxtLink class="lang" @click.prevent="setLocale('de')" :class="{ 'active': locale === 'de' }">DE</NuxtLink>
          </div>
        </div>
      </div>
      </div>
  </div>
</template>
<script setup>
const { setLocale, locale } = useI18n();
import { useRoute } from 'vue-router'
import { useLocalePath } from '#imports'
const localePath = useLocalePath()
const route = useRoute()

// funkcja sprawdzająca, czy jesteśmy na stronie głównej
const isHomePage = computed(() => {
  // dla stron z prefiksem języka, np. /en lub /de
  const path = route.path.replace(/^\/(en|de)/, '')
  return path === '/' || path === ''
})
</script>