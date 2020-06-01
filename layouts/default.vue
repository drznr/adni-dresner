<template>
    <div>
        <main-navbar />
        <nuxt />
        <main-footer />
    </div>
</template>

<script>
import mainNavbar from '@/components/main-navbar'
import mainFooter from '@/components/main-footer'

export default {
    components: {
        mainNavbar,
        mainFooter
    }
}
</script>
