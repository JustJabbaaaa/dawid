<template>
    <Navbar />
    <Section anchor="impressum" class="impressum">
        <h1>{{ $t('impressum.title') }}</h1>

        <section class="company">
            <h2>{{ $t('impressum.company.line1') }}</h2>
            <p>{{ $t('impressum.company.line2') }}</p>
            <p>{{ $t('impressum.company.line3') }}</p>
            <p>{{ $t('impressum.company.line4') }}</p>
            <p>{{ $t('impressum.company.line5') }}</p>
            <p>E-Mail: info@heiko-zillmann.de</p>
            <p>{{ $t('impressum.company.line7') }}</p>
        </section>

        <section class="responsible">
            <h2>{{ $t('impressum.responsible.line1') }}</h2>
            <p>{{ $t('impressum.responsible.line2') }}</p>
            <p>{{ $t('impressum.responsible.line3') }}</p>
            <p>{{ $t('impressum.responsible.line4') }}</p>
        </section>

        <section class="text">
            <p>{{ $t('impressum.liability') }}</p>
            <p>{{ $t('impressum.links') }}</p>
            <p>{{ $t('impressum.copyright') }}</p>
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