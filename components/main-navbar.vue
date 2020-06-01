<template>
    <section class="main-navbar">
        <div class="container">
            <h1>
                <nuxt-link to="/">
                    צבי דרזנר ושות'
                </nuxt-link>
            </h1>
            <nav>
                <span class="contacts">
                    <span>
                        <font-awesome-icon icon="phone-alt" />
                        03-6131334
                    </span>
                    <a href="mailto:dresner@dresner.co.il">
                        <font-awesome-icon icon="envelope" />
                        dresner@dresner.co.il
                    </a>
                </span>
                <ul v-hammer:swipe.right="closeNav" class="nav" :class="{ open: isMenuOpen }">
                    <nuxt-link to="/" class="nav-link" @click.native="closeNav">
                        דף הבית
                    </nuxt-link>
                    <nuxt-link to="/about" class="nav-link" @click.native="closeNav">
                        אודות המשרד
                    </nuxt-link>
                    <nuxt-link to="/stuff" class="nav-link" @click.native="closeNav">
                        סגל
                    </nuxt-link>
                    <nuxt-link to="/expertises" class="nav-link" @click.native="closeNav">
                        תחומי התמחות
                    </nuxt-link>
                    <nuxt-link to="/accomplishments" class="nav-link" @click.native="closeNav">
                        הישגים
                    </nuxt-link>
                </ul>
            </nav>
            <hamburger-toggle class="main-navbar-toggle" :is-menu-open="isMenuOpen" @menu-toggle="isMenuOpen = !isMenuOpen" />
        </div>
    </section>
</template>

<script>
import hamburgerToggle from './hamburger-toggle'

export default {
    components: {
        hamburgerToggle
    },
    data () {
        return {
            isMenuOpen: false
        }
    },
    methods: {
        closeNav () {
            this.isMenuOpen = false
        }
    }
}
</script>
