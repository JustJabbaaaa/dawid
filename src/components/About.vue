<template>
  <Section anchor="About">
     <div
      class="about"
      :class="{ expanded: showMore }"
      ref="aboutSection"
    >
      <div class="about__content">
        <div class="about__content--header">
          <span>
            There are people who don’t seek the spotlight –
            they create impact quietly, steadily, with integrity
            and responsibility.
          </span>
        </div>
        <div class="about__content--imgText">
          <NuxtImg src="/images/about/about_photo.webp"/>
          <div class="about__content--description">
            <p class="about__content--para">
              Born and raised is Oranienburg, deeply rooted in his hometown,
              Heiko has earned the trust and respect of the community
              over decades – not through consistent action. Through reliability.
              Through closeness to the people.
            </p>
            <p class="about__content--text">
              For more than 25 years, Heiko Zillmann has been active as
              an entrepreneur – in real estate, HR services, and the service
              sector. He built companies, created jobs, connected people,
              and provided solutions where others only saw problems.
              His perspective has always been grounded: focused on what’s
              practically achievable – and morally right
            </p>
            <p v-if="showMore" class="about__content--text">
                Heiko’s commitment to his hometown goes beyond business. He supports local initiatives, mentors young entrepreneurs, and is always ready to lend a helping hand. His story is one of dedication, humility, and a deep sense of responsibility to his community.
            </p>
            <NuxtLink
              class="about__content--readMore"
              @click.prevent="toggleReadMore"
              :class="{ active: showMore }"
            >
              <div>{{ showMore ? 'read less' : 'read more' }}</div>
              <NuxtImg src="/images/about/arrow_down.svg"/>
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