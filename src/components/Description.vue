<template>
    <Section anchor="Description" class="description" grid="2">
        <div class="column">
            <NuxtImg src="/images/description/text.svg"/>
            <h2>{{ $t('description.left.title.first') }}<br/>{{ $t('description.left.title.second') }}</h2>
            <p>{{ $t('description.left.para1') }}</p>
            <p>{{ $t('description.left.para2') }}</p>
        </div>
        <div class="column">
            <div class="images">
                <div class="photos">
                    <NuxtImg src="/images/description/heiko.webp"/>
                    <NuxtImg src="/images/description/tower.webp"/>
                    <div class="other">
                        <div class="placeholder"></div>
                        <NuxtImg src="/images/description/herb.webp" class="herb"/>
                    </div>
                </div>
                
            </div>
            <p>{{ $t('description.right.para1') }}</p>
            <p>{{ $t('description.right.para2') }}</p>
        </div>
    </Section>
</template>