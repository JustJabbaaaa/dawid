<template>
    <Section anchor="Vision" class="vision" grid="2">
        <div class="column">
            <h1>"{{ $t('vision.quote.first') }} {{ $t('vision.quote.second') }} {{ $t('vision.quote.third') }} {{ $t('vision.quote.fourth') }}"</h1>
            <h2>{{ $t('vision.left.title.first') }} {{ $t('vision.left.title.second') }}</h2>
            <p>{{ $t('vision.left.para1') }}</p>
            <p>{{ $t('vision.left.para2') }}</p>
        </div>
        <div class="column">
            <div class="images">
                <div class="photos">
                    <NuxtImg src="/images/vision/heiko.webp"/>
                    <NuxtImg src="/images/vision/tower.webp"/>
                    <div class="other">
                        <div class="placeholder"></div>
                        <NuxtImg src="/images/vision/herb.webp" class="herb"/>
                    </div>
                </div>
                
            </div>
            <p>{{ $t('vision.right.para1') }}</p>
            <p>{{ $t('vision.right.para2') }}</p>
        </div>
    </Section>
</template>