<template>
    <Section anchor="Vision" class="vision" grid="2">
        <div class="column">
            <h2>{{ $t('vision.left.title.first') }}</h2>
            <p>{{ $t('vision.left.para1') }}</p>
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
        </div>
    </Section>
</template>