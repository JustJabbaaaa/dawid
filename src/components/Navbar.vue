<template>
  <div id="Navbar">
    <div class="nav">
      <NuxtLink to="/" class="nav__brand" aria-label="Go to homepage">
        {{ $t('navbar.logo.yourCandidate') }}<br/>{{ $t('navbar.logo.mayor') }}<br class="linebreak" v-if="$i18n.locale === 'de'" /> <NuxtImg src="/images/vision/herb.webp"/><span>Oranienburg</span></NuxtLink>
      <div class="nav__buttons">
        <div class="nav__buttons--navMenu">
          <li class="nav__buttons--item"><NuxtLink to="#About" class="nav__buttons--btn">{{ $t('navbar.links.about') }}</NuxtLink></li>
          <li class="nav__buttons--item"><NuxtLink to="#Footer" class="nav__buttons--btn">{{ $t('navbar.links.support') }}</NuxtLink></li>
          <li class="nav__buttons--item"><NuxtLink to="#Contact" class="nav__buttons--btn">{{ $t('navbar.links.contact') }}</NuxtLink></li>
        </div>
        <div class="nav__buttons--navSocials">
          <div class="socials">
            <NuxtLink to=""><NuxtImg src="images/navbar/twitter.svg" alt="twitter" class="social"/></NuxtLink>
            <NuxtLink to=""><NuxtImg src="images/navbar/fb.svg" alt="facebook" class="social"/></NuxtLink>
            <NuxtLink to=""><NuxtImg src="images/navbar/insta.svg" alt="instagram" class="social"/></NuxtLink>
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
</script>