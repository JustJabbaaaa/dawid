<template>
  <Section anchor="About">
     <div
      class="about"
      :class="{ expanded: showMore }"
      ref="aboutSection"
      >    
        <div class="about__title">
          <h2>{{ $t('about.title') }}</h2>
        </div>
          <div class="about__content">
            <div class="about__content--imgText">
              <div class="about__content--top">
                <div class="about__content--header">
                  <span>
                    {{ $t('about.header') }}
                  </span>
                </div>
                <NuxtImg class="photo" src="/images/about/about_photo.webp"/>
              </div>
              <div class="about__content--description">
                <p class="about__content--text">
                  {{ $t('about.para1') }}
                </p>
                <p class="about__content--text">
                  {{ $t('about.para2') }}
                </p>
                <div
                  class="about__content--expandable"
                  :class="{ expanded: showMore }"
                >
                  <p class="about__content--text">
                    {{ $t('about.paraExpanded') }}
                  </p>
                </div>
                <NuxtLink
                  class="about__content--readMore"
                  @click.prevent="toggleReadMore"
                  :class="{ active: showMore }"
                >
                  <div>{{ showMore ? $t("about.btn.readLess") : $t("about.btn.readMore") }}</div>
                  <NuxtImg src="/images/about/arrow.svg"/>
                </NuxtLink>
              </div>
            </div>
          </div>
      </div>
  </Section>
</template>
<script setup>
import { ref } from 'vue'

const showMore = ref(false)

function toggleReadMore() {
  showMore.value = !showMore.value
}
</script>