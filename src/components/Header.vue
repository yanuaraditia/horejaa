<template>
    <b-navbar v-bind:data-scroll="isScroll">
        <template slot="brand">
            <b-navbar-item tag="router-link" :to="{ path: '/' }">
                <g-image :alt="$static.metadata.siteName" src="~/images/horekaa.png" width="120px"></g-image>
            </b-navbar-item>
        </template>
        <!-- <template slot="start">
            <b-navbar-item tag="router-link" :to="{ path: '/product' }">
                Product
            </b-navbar-item>
            <b-navbar-item tag="router-link" :to="{ path: '/about' }">
                About
            </b-navbar-item>
        </template> -->
        <template slot="end">
            <b-navbar-item tag="div">
                <div class="buttons">
                    <a href="mailto:kharisma.fr@gmail.com" class="button is-outlined has-text-primary">Hubungi Kami</a>
                    <!-- <g-link class="button is-outlined has-text-primary" to="/register">Get Started</g-link> -->
                </div>
            </b-navbar-item>
        </template>
    </b-navbar>
</template>
<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>
<script>
export default {
    data() {
        return {
            isScroll: false,
            lastScrollPosition: 0,
        }
    },
    methods: {
        scrollFunction() {
            const currentScrollPosition = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop
            if(currentScrollPosition < 0) {
                this.isScroll = true
                return 
            }
            if(Math.abs(currentScrollPosition - this.lastScrollPosition) < 60) {
                this.isScroll = true
                return
            }
            this.isScroll = false
            this.lastScrollPosition = currentScrollPosition
            console.log(this.lastScrollPosition)
        }
    },
    destroyed() {
        window.removeEventListener('scroll',this.scrollFunction())
    },
    mounted() {
        window.addEventListener('scroll',this.scrollFunction())
    }
}
</script>