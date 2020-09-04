<template>
    <Layout>
        <Jumbotron title="Tidak Ditemukan" description="Sedang kami siapkan 😊"/>
    </Layout>
</template>

<script>
import Jumbotron from '~/components/Jumbotron.vue'

export default {
    components: {
        Jumbotron,
    },
    metaInfo: {
        title: '404 Not Found'
    }
}
</script>