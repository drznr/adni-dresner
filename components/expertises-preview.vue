<template>
    <section class="expertises-preview">
        <main class="container">
            <div v-for="(exp, idx) in expertises" :key="idx" class="expertises-preview-item">
                <nuxt-link to="/expertises">
                    <img :src="require(`~/assets/imgs/${exp.icon}.svg`)" alt="icon">
                    <h4>{{ exp.txt }}</h4>
                </nuxt-link>
            </div>
        </main>
    </section>
</template>

<script>
export default {
    data () {
        return {
            expertises: [
                { txt: 'הוצאה לפועל וחדלות פירעון', icon: 'poor' },
                { txt: 'בנקאות', icon: 'bank' },
                { txt: 'מקרקעין', icon: 'real-estate' },
                { txt: 'ליטיגציה מסחרית', icon: 'litigation' },
                { txt: 'הגנת הדייר', icon: 'rent' },
                { txt: 'חוזים מסחריים', icon: 'contract' },
                { txt: 'צוואות וירושות', icon: 'will' }
            ]
        }
    }
}
</script>
