<template>
  <Layout>
    <section class="section">
      <div class="container is-fluid">
        <div class="columns">
          <div class="column is-6-desktop">
            <g-image alt="Example image" src="~/favicon.png" width="135" />
            <h1 class="title is-1"><span class="has-text-weight-normal">Permudah bisnis anda dengan aplikasi</span> Horejaa</h1>
            <p class="subtitle font-primary">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur excepturi labore tempore expedita, et iste tenetur suscipit explicabo! Dolores, aperiam non officia eos quod asperiores
            </p>
            <p class="home-links">
              <g-link to="/about" class="button is-primary is-rounded">Tentang Kami</g-link>
              <button type="button" class="button is-outlined is-primary is-rounded" @click="showForm()">Daftar</button>
            </p>
          </div>
          <div class="column is-6-desktop">
            <g-image src="~/images/banner-front.jpg" width="400px" blur="3" class="float-right"></g-image>
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
      email: null
    }
  },
  metaInfo: {
    title: 'Beranda'
  },
  methods: {
    showForm() {
      var mail = prompt("Harap masukkan e-mail perusahaan anda:")
      if(mail == null || mail == "") {
        this.email = null
      } else {
        this.email = mail
      }
    }
  }
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
