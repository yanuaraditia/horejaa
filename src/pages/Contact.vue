<template>
    <Layout>
        <section class="hero is-medium">
            <div class="hero-body">
                <div class="container">
                    <div class="columns">
                        <div class="column is-12-mobile is-6-desktop">
                            <h1 class="title is-1">Contact Us</h1>
                            <p>We’re here to help, with 24/7 outstanding support. Ask us about the product, the free trial, our resources or features. Whatever you need help with.</p>
                            <div class="m-5"></div>
                            <strong>Horejaa address</strong>
                            <p>Jl. Watugede No.58, Sariharjo, Ngaglik, Kabupaten Sleman, <br/>Daerah Istimewa Yogyakarta 55581</p>
                        </div>
                        <div class="column is-12-mobile is-6-desktop">
                            <form>
                                <b-field label="Nama Lengkap">
                                    <b-input maxlength="70" type="text"></b-input>
                                </b-field>
                                <div class="columns is-flex">
                                    <div class="column is-6">
                                        <b-field label="E-mail">
                                            <b-input maxlength="70" type="text"></b-input>
                                        </b-field>
                                    </div>
                                    <div class="column is-6">
                                        <b-field label="Nomor Telepon">
                                            <b-input maxlength="70" type="text"></b-input>
                                        </b-field>
                                    </div>
                                </div>
                                <b-field label="Nama Perusahaan">
                                    <b-input maxlength="70" type="text"></b-input>
                                </b-field>
                                <b-field label="Message">
                                    <b-input maxlength="200" type="textarea"></b-input>
                                </b-field>
                                <button class="button is-primary is-fullwidth is-medium" v-on:click="send" v-if="isSend" type="button">Contact Us</button>
                                <b-button class="is-medium is-fullwidth is-primary" v-else loading>Contact Us</b-button>
                            </form>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </Layout>
</template>
<script>
export default {
    data() {
        return {
            isSend: true
        }
    },
    methods: {
        send() {
            this.isSend = false
            setInterval(() => {
                this.isSend = true
            }, 1000);
        }
    }
}
</script>