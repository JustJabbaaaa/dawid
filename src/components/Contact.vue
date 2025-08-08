<template>
  <Section anchor="Contact" class="contact">
    <div class="contact__wrapper">
      <h2>{{ $t('contact.title') }}</h2>

      <form @submit.prevent="handleSubmit" class="contact__form">
        <!-- Name -->
        <div class="form-group">
          <label for="name">{{ $t('contact.name') }} <span class="required">*</span></label>
          <input id="name" v-model="form.name" type="text" required />
        </div>

        <!-- Email -->
        <div class="form-group">
          <label for="email">{{ $t('contact.email') }} <span class="required">*</span></label>
          <input id="email" v-model="form.email" type="email" required />
        </div>

        <!-- Message -->
        <div class="form-group">
          <label for="message">{{ $t('contact.message') }} <span class="required">*</span></label>
          <textarea id="message" v-model="form.message" required rows="5"></textarea>
        </div>

        <!-- Consent -->
        <div class="form-consent">
          <input id="consent" v-model="form.consent" type="checkbox" required />
          <label for="consent">
            {{ $t('contact.consent') }}
            <button type="button" class="link-btn" @click="showPrivacy = true">
              {{ $t('contact.privacyPolicy') }}
            </button>
          </label>
        </div>

        <!-- Submit Button -->
        <button type="submit" :disabled="loading">
          {{ loading ? $t('contact.sending') : $t('contact.submit') }}
        </button>

        <!-- Success / Error Messages -->
        <p v-if="successMessage" class="message success">{{ successMessage }}</p>
        <p v-if="errorMessage" class="message error">{{ errorMessage }}</p>
      </form>
    </div>

    <!-- Privacy Policy Modal -->
    <div v-if="showPrivacy" class="modal-overlay" @click.self="showPrivacy = false">
  <div class="modal" role="dialog" aria-modal="true" aria-labelledby="privacy-title">
    <header>
      <h3 id="privacy-title">{{ $t('privacy.title') }}</h3>
      <button class="close-btn" @click="showPrivacy = false" aria-label="Close modal">&times;</button>
    </header>
    <div class="modal-content">
      <p>{{ $t('privacy.intro') }}</p>
      <h4>{{ $t('privacy.dataCollectionTitle') || 'Datenerhebung' }}</h4>
      <p>{{ $t('privacy.dataCollection') }}</p>

      <h4>{{ $t('privacy.cookiesTitle') || 'Cookies' }}</h4>
      <p>{{ $t('privacy.cookies') }}</p>

      <h4>{{ $t('privacy.dataProtectionRightsTitle') || 'Ihre Rechte' }}</h4>
      <p>{{ $t('privacy.dataProtectionRights') }}</p>

      <h4>{{ $t('privacy.legalBasisTitle') || 'Rechtsgrundlage' }}</h4>
      <p>{{ $t('privacy.legalBasis') }}</p>

      <h4>{{ $t('privacy.contactTitle') || 'Kontakt' }}</h4>
      <p>{{ $t('privacy.contact') }}</p>
    </div>
    <footer>
      <button @click="showPrivacy = false">{{ $t('privacy.close') }}</button>
    </footer>
  </div>
</div>
  </Section>
</template>

<script setup>
import { ref } from 'vue'
import { useI18n } from 'vue-i18n'

const { t } = useI18n()

// Twój endpoint Formspree
const FORMSPREE_URL = 'https://formspree.io/f/xnnzoebp'

const form = ref({
  name: '',
  email: '',
  message: '',
  consent: false
})

const loading = ref(false)
const successMessage = ref('')
const errorMessage = ref('')
const showPrivacy = ref(false)

const handleSubmit = async () => {
  loading.value = true
  successMessage.value = ''
  errorMessage.value = ''

  try {
    const res = await fetch(FORMSPREE_URL, {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify(form.value)
    })

    if (res.ok) {
      successMessage.value = t('contact.success')
      form.value = { name: '', email: '', message: '', consent: false }
    } else {
      throw new Error('Form error')
    }
  } catch (err) {
    errorMessage.value = t('contact.error')
  } finally {
    loading.value = false
  }
}
</script>
