<template>
  <Layout>
    <section class="hero is-medium has-text-centered">
      <div class="hero-body">
        <div class="w-50-lg">
          <h2 class="title is-2">We help ecommerce businesses be more successful online</h2>
          <p class="m-5">With simple, fast, and affordable fulfillment.</p>
          <button class="button is-link border-aqua has-text-primary" type="button">Company</button>
          <button class="button is-link border-aqua has-text-primary" type="button">Leadership</button>
          <button class="button is-link border-aqua has-text-primary" type="button">Careers</button>
        </div>
      </div>
    </section>
    <section class="section">
      <div class="container">
        <div class="columns is-flex">
          <div class="column is-12-mobile is-3-desktop">
            <div class="card people-card">
              <div class="card-image">
                <figure class="image is-1by1">
                  <g-image src="~/images/people/people1.jpg" fit="cover" blur="5"/>
                </figure>
              </div>
              <div class="card-content">
                <h2 class="title is-5">John Smith</h2>
                <p class="subtitle is-6">Kuli</p>
              </div>
            </div>
          </div>
          <div class="column is-12-mobile is-3-desktop">
            <div class="card people-card">
              <div class="card-image">
                <figure class="image is-1by1">
                  <g-image src="~/images/people/people1.jpg" fit="cover" blur="5"/>
                </figure>
              </div>
              <div class="card-content">
                <h2 class="title is-5">John Smith</h2>
                <p class="subtitle is-6">Kuli</p>
              </div>
            </div>
          </div>
          <div class="column is-12-mobile is-3-desktop">
            <div class="card people-card">
              <div class="card-image">
                <figure class="image is-1by1">
                  <g-image src="~/images/people/people1.jpg" fit="cover" blur="5"/>
                </figure>
              </div>
              <div class="card-content">
                <h2 class="title is-5">John Smith</h2>
                <p class="subtitle is-6">Kuli</p>
              </div>
            </div>
          </div>
          <div class="column is-12-mobile is-3-desktop">
            <div class="card people-card">
              <div class="card-image">
                <figure class="image is-1by1">
                  <g-image src="~/images/people/people1.jpg" fit="cover" blur="5"/>
                </figure>
              </div>
              <div class="card-content">
                <h2 class="title is-5">John Smith</h2>
                <p class="subtitle is-6">Kuli</p>
              </div>
            </div>
          </div>
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
