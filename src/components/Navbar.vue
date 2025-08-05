<template>
  <div id="Navbar">
    <div class="nav">
      <NuxtLink to="/" class="nav__brand" aria-label="Go to homepage">
        Your Candidate for<br/>Mayor of <NuxtImg src="/images/description/herb.webp"/><span>Oranienburg</span></NuxtLink>
      <div class="nav__buttons">
        <div class="nav__buttons--navMenu">
          <li class="nav__buttons--item"><NuxtLink to="#" class="nav__buttons--btn">About</NuxtLink></li>
          <li class="nav__buttons--item"><NuxtLink to="#" class="nav__buttons--btn">Vision</NuxtLink></li>
          <li class="nav__buttons--item"><NuxtLink to="#" class="nav__buttons--btn">Contact</NuxtLink></li>
        </div>
        <div class="nav__buttons--navSocials">
          <div class="socials">
          <NuxtImg src="images/navbar/twitter.svg" alt="facebook" class="social"/>
          <NuxtImg src="images/navbar/fb.svg" alt="facebook" class="social"/>
          <NuxtImg src="images/navbar/insta.svg" alt="facebook" class="social"/>
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