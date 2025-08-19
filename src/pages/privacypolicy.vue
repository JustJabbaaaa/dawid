<template>
    <Navbar />
    <Section anchor="PrivacyPolicy" class="privacy-policy">
        <h1>{{ $t('privacy.title') }}</h1>
        <ol>
            <li>
                <h3>{{ $t('privacy.general.header') }}</h3>
                <p>{{ $t('privacy.general.text') }}</p>
            </li>
            <li>
                <h3>{{ $t('privacy.responsible.header') }}</h3>
                <ul class="nonumered">
                    <li>{{ $t('privacy.responsible.line1') }}</li>
                    <li>{{ $t('privacy.responsible.line2') }}</li>
                    <li>{{ $t('privacy.responsible.line3') }}</li>
                    <li>{{ $t('privacy.responsible.line4') }}</li>
                </ul>
            </li>
            <li>
                <h3>{{ $t('privacy.data_collection.header') }}</h3>
                <p>{{ $t('privacy.data_collection.text') }}</p>
            </li>
            <li>
                <h3>{{ $t('privacy.cookies.header') }}</h3>
                <p>{{ $t('privacy.cookies.text') }}</p>
            </li>
            <li>
                <h3>{{ $t('privacy.server_logs.header') }}</h3>
                <p>{{ $t('privacy.server_logs.text') }}</p>
            </li>
            <li>
                <h3>{{ $t('privacy.contact_form.header') }}</h3>
                <p>{{ $t('privacy.contact_form.text') }}</p>
            </li>
            <li>
                <h3>{{ $t('privacy.plugins_tools.header') }}</h3>
                <p>{{ $t('privacy.plugins_tools.text') }}</p>
            </li>
            <li>
                <h3>{{ $t('privacy.rights.header') }}</h3>
                <p>{{ $t('privacy.rights.text') }}</p>
            </li>
            <li>
                <h3>{{ $t('privacy.complaints.header') }}</h3>
                <p>{{ $t('privacy.complaints.text') }}</p>
            </li>
            <li>
                <h3>{{ $t('privacy.ssl.header') }}</h3>
                <p>{{ $t('privacy.ssl.text') }}</p>
            </li>
        </ol>
    </Section>
    <Footer />
</template>
<style scoped>
body{
    min-height:80vh;
}
li{
    list-style-type:decimal;
    font-size:1.75rem;
}
h1{
    font-size:2.5rem;
    margin-bottom:.75rem;
}
.nonumered li{
    list-style-type:none;
    font-size:1rem;
}
h2{
    font-size:1.75rem;
    margin-bottom:.5rem;
}
 p{
    font-size:1rem;
    margin-bottom:1rem;
 }
 section{
    margin-bottom:2rem;
 }
</style>