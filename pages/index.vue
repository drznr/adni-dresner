<template>
    <section>
        <main-header />
        <about-preview />
        <expertises-preview />
        <stuff-preview />
    </section>
</template>

<script>
import mainHeader from '@/components/main-header'
import expertisesPreview from '@/components/expertises-preview'
import aboutPreview from '@/components/about-preview'
import stuffPreview from '@/components/stuff-preview'

export default {
    components: {
        mainHeader,
        expertisesPreview,
        aboutPreview,
        stuffPreview
    }
}
</script>
