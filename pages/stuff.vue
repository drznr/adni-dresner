<template>
    <section class="stuff-page">
        <header>
            <img src="~/assets/imgs/hero.jpg" alt="header background image" class="hero-small">
        </header>
        <main class="container">
            <h2>הצוות שלנו</h2>
            <div v-for="(lawyer, idx) in lawyers" :key="idx" class="stuff-page-lawyer">
                <img :src="require(`~/assets/imgs/${lawyer.img}`)" alt="lawyer's image">
                <div class="stuff-page-lawyer-details">
                    <h3>{{ lawyer.name }}</h3>
                    <p v-if="lawyer.isMain">
                        <img :src="require(`~/assets/imgs/${lawyer.img}`)" alt="lawyer's image">
                        {{ lawyer.txt }}
                    </p>
                    <a href="mailto:example@example.com" target="_blank">example@example.com</a>
                </div>
            </div>
        </main>
    </section>
</template>

<script>
export default {
    data () {
        return {
            lawyers: [
                { name: 'עו"ד אביחי דרזנר', img: 'lawyer1.jpg', isMain: true, txt: 'לורם איפסום דולור סיט אמט, קונסקטורר אדיפיסינג אלית לורם איפסום דולור סיט אמט, קונסקטורר אדיפיסינג אלית. סת אלמנקום ניסי נון ניבאה. דס איאקוליס וולופטה דיאם. וסטיבולום אט דולור, קראס אגת לקטוס וואל אאוגו וסטיבולום סוליסי טידום בעליק. קולורס מונפרד אדנדום סילקוף, מרגשי ומרגשח. עמחליף סחטיר בלובק. תצטנפל בלינדו למרקל אס לכימפו, דול, צוט ומעיוט - לפתיעם ברשג - ולתיעם גדדיש.' },
                { name: 'עו"ד נמרוד דרזנר', img: 'lawyer2.jpg', isMain: true, txt: 'לורם איפסום דולור סיט אמט, קונסקטורר אדיפיסינג אלית לורם איפסום דולור סיט אמט, קונסקטורר אדיפיסינג אלית. סת אלמנקום ניסי נון ניבאה. דס איאקוליס וולופטה דיאם. וסטיבולום אט דולור, קראס אגת לקטוס וואל אאוגו וסטיבולום סוליסי טידום בעליק. קולורס מונפרד אדנדום סילקוף, מרגשי ומרגשח. עמחליף סחטיר בלובק. תצטנפל בלינדו למרקל אס לכימפו, דול, צוט ומעיוט - לפתיעם ברשג - ולתיעם גדדיש.' },
                { name: 'עו"ד הדס בר-און', img: 'lawyer3.jpg', isMain: true, txt: 'לורם איפסום דולור סיט אמט, קונסקטורר אדיפיסינג אלית לורם איפסום דולור סיט אמט, קונסקטורר אדיפיסינג אלית. סת אלמנקום ניסי נון ניבאה. דס איאקוליס וולופטה דיאם. וסטיבולום אט דולור, קראס אגת לקטוס וואל אאוגו וסטיבולום סוליסי טידום בעליק. קולורס מונפרד אדנדום סילקוף, מרגשי ומרגשח. עמחליף סחטיר בלובק. תצטנפל בלינדו למרקל אס לכימפו, דול, צוט ומעיוט - לפתיעם ברשג - ולתיעם גדדיש.' },
                { name: 'עו"ד ישראל ישראלי', img: 'lawyer4.jpg', isMain: false },
                { name: 'עו"ד ישראל ישראלי', img: 'lawyer5.jpg', isMain: false }
            ]
        }
    }
}
</script>
