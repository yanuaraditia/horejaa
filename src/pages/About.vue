<template>
  <Layout>
    <section class="hero is-medium has-text-centered">
      <div class="hero-body">
        <div class="w-50-lg">
          <h2 class="title is-2">We help ecommerce businesses be more successful online</h2>
          <p class="m-5">With simple, fast, and affordable fulfillment.</p>
          <!-- <button class="button is-link border-aqua has-text-primary" type="button">Company</button>
          <button class="button is-link border-aqua has-text-primary" type="button">Leadership</button>
          <button class="button is-link border-aqua has-text-primary" type="button">Careers</button> -->
        </div>
      </div>
    </section>
    <Cta/>
  </Layout>
</template>

<script>
import Cta from '~/components/Cta.vue'
export default {
  components: {
    Cta,
  },
  metaInfo: {
    title: 'Tentang'
  },
  data() {
    return {
      dummy: [
        {
          id: 1,
          name: 'Joni',
          position: 'CEO'
        },
        {
          id: 2,
          name: 'Eko',
          position: 'CFO'
        },
        {
          id: 3,
          name: 'Agus',
          position: 'CTO'
        },
        {
          id: 4,
          name: 'Paijem',
          position: 'VP Engineer'
        },
      ]
    }
  }
}
</script>

<style lang="scss">
.people-card {
  box-shadow: none;
  .card-content {
    padding: 1rem 0;
  }
}
</style>
