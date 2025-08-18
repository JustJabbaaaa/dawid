<template>
    <Navbar />
    <Section anchor="PrivacyPolicy" class="privacy-policy">
        <h1>{{ $t('privacy.title') }}</h1>

        <section class="general">
        <p>{{ $t('privacy.general') }}</p>
        </section>

        <section class="responsible">
            <h2>{{ $t('privacy.responsible.line1') }}</h2>
            <p>{{ $t('privacy.responsible.line2') }}</p>
            <p>{{ $t('privacy.responsible.line3') }}</p>
            <p>{{ $t('privacy.responsible.line4') }}</p>
            <p>Email: info@heiko-zillmann.de</p>
        </section>

        <section class="text">
            <p>{{ $t('privacy.data_collection') }}</p>
            <p>{{ $t('privacy.cookies') }}</p>
            <p>{{ $t('privacy.server_logs') }}</p>
            <p>{{ $t('privacy.contact_form') }}</p>
            <p>{{ $t('privacy.plugins_tools') }}</p>
            <p>{{ $t('privacy.rights') }}</p>
            <p>{{ $t('privacy.complaints') }}</p>
            <p>{{ $t('privacy.ssl') }}</p>
        </section>
    </Section>
    <Footer />
</template>
<style scoped>
body{
    min-height:80vh;
}
h1{
    font-size:2.5rem;
    margin-bottom:.75rem;
}
h2{
    font-size:1.75rem;
    margin-bottom:.5rem;
}
 p{
    margin-bottom:1rem;
 }
 section{
    margin-bottom:2rem;
 }
</style>