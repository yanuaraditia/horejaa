<template>
    <Layout>
        <section class="section is-medium">
            <div class="container is-small">
                            <form>
                                <b-field label="Nama Lengkap">
                                    <b-input
                                     v-model="form.fullName"
                                     maxlength="70"
                                     minlength="5"
                                     type="text"></b-input>
                                </b-field>
                                <div class="columns is-flex">
                                    <div class="column is-6">
                                        <b-field label="E-mail">
                                            <b-input
                                             v-model="form.email"
                                             maxlength="70"
                                             minlength="5"
                                             type="email"></b-input>
                                        </b-field>
                                    </div>
                                    <div class="column is-6">
                                        <b-field label="Nomor Telepon">
                                            <b-input
                                             v-model="form.phone"
                                             maxlength="70"
                                             minlength="5"
                                             placeholder="08xxx"
                                             type="text"></b-input>
                                        </b-field>
                                    </div>
                                </div>
                                <b-field label="Nama Perusahaan">
                                    <b-input maxlength="70" v-model="form.compName" type="text"></b-input>
                                </b-field>
                                <b-field label="Message">
                                    <b-input maxlength="200" v-model="form.message" type="textarea"></b-input>
                                </b-field>
                                <button class="button is-primary is-fullwidth is-medium" v-on:click="send" v-if="isSend" type="button">Contact Us</button>
                                <b-button class="is-medium is-fullwidth is-primary" v-else loading>Contact Us</b-button>
                            </form> 
            </div>
        </section>
    </Layout>
</template>
<script>
export default {
    data() {
        return {
            isSend: true,
            form: {
                fullName: null,
                email: null,
                phone: null,
                compName: null,
                message: null
            },
        }
    },
    metaInfo: {
        title: 'Contact Us'
    },
    methods: {
        send() {
            if(
                this.form.fullName == null ||
                this.form.email == null ||
                this.form.phone == null ||
                this.form.compName == null ||
                this.form.message == null
            ) {
                this.danger('Cok isi sek')
                return
            }
            this.isSend = false
            setInterval(() => {
                this.isSend = true
            }, 1000)

            this.success('Joss')
            this.clear()
        },
        danger(title) {
            this.$buefy.toast.open({
                duration: 500,
                message: title,
                position: 'is-bottom',
                type: 'is-danger'
            })
        },
        success(title) {
            this.$buefy.toast.open({
                duration: 500,
                message: title,
                position: 'is-bottom',
                type: 'is-success'
            })
        },
        clear() {
            this.form.fullName = null
            this.form.email = null
            this.form.phone = null
            this.form.compName = null
            this.form.message = null
        }
    }
}
</script>