<template>
    <section class="hero is-primary has-text-centered">
        <div class="hero-body">
            <div class="container is-fluid">
                <div class="columns">
                    <div class="column is-8-desktop has-text-left-desktop">
                        <p>TEMUKAN KEMUDAHAN DALAM BERBISNIS.</p>
                        <h2 class="title is-2">Siap mempermudah bisnis anda dengan kami?</h2>
                    </div>
                    <div class="column is-4-desktop has-text-right-desktop">
                        <g-link to="/register" class="button is-white has-text-primary is-rounded mat">Coba Sekarang</g-link>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<style lang="scss">
.mat {
    @media screen and (min-width: 992px) {
        margin-top: 35px;
    }
}
</style>