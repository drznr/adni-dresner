<template>
    <section class="stuff-preview container">
        <h2>הצוות שלנו</h2>
        <main>
            <nuxt-link v-for="(lawyer, idx) in lawyers" :key="idx" to="/stuff">
                <div class="stuff-preview-card">
                    <figure>
                        <img :src="require(`~/assets/imgs/${lawyer.img}`)" alt="lawyer's image">
                    </figure>
                    <h4>{{ lawyer.name }}</h4>
                    <span>קרא עוד...</span>
                </div>
            </nuxt-link>
        </main>
    </section>
</template>

<script>
export default {
    data () {
        return {
            lawyers: [
                { name: 'עו"ד אביחי דרזנר', img: 'lawyer1.jpg' },
                { name: 'עו"ד נמרוד דרזנר', img: 'lawyer2.jpg' },
                { name: 'עו"ד הדס בר-און', img: 'lawyer3.jpg' },
                { name: 'עו"ד ישראל ישראלי', img: 'lawyer4.jpg' },
                { name: 'עו"ד ישראל ישראלי', img: 'lawyer5.jpg' }
            ]
        }
    }
}
</script>
