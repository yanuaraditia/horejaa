<template>
  <Layout>
    <section class="section">
      <div class="container is-fluid">
        <div class="columns">
          <div class="column is-6-desktop">
            <h1 class="title is-1 is-4-mobile" style="margin-bottom: 3rem">Dipetik, dikemas,<br/> dan dikirim.</h1>
            <p class="subtitle font-primary">Horeja adalah aplikasi yang dikembangkan dibawah bisnis Palagan Food Supplier. Aplikasi ini dibuat dengan tujuan untuk mempermudah pemesanan barang, didukung dengan beberapa fitur unggulan serta katalog barang yang lengkap sehingga memenuhi kebutuhan bisnis horeka Anda.</p>
            <p class="subtitle font-primary">Dengan layanan pemenuhan yang andal, gudang di dekat pelanggan Anda, dan teknologi terhubung yang mendukung jaringan pemenuhan kami, kami membantu meningkatkan waktu transit, biaya pengiriman, dan pengalaman pengiriman bagi pelanggan Anda.</p>
            <p class="home-links">
              <g-link to="/register" class="button is-primary is-medium is-rounded">Coba Sekarang</g-link>
            </p>
          </div>
          <div class="column is-6-desktop">
            <div class="lander">
              <g-image src="~/images/banner-front.jpg" width="400px" blur="3"></g-image>
              <blockquote>
                <p>"Kami telah melihat penghematan biaya 25,3% sejak beralih ke Horejaa, karena kami menggunakan tiga pusat pemenuhan mereka."</p>
              </blockquote>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="section">
      <div class="container is-fluid">
        <div class="columns is-multiline is-flex">
          <div class="column is-6-mobile is-3-desktop has-text-centered">
            <h3 class="title is-1">99.91%</h3>
            <h5 class="subtitle is-6">Akurasi tinggi</h5>
          </div>
          <div class="column is-6-mobile is-3-desktop has-text-centered">
            <h3 class="title is-1">3.500+</h3>
            <h5 class="subtitle is-6">Produk telah tersalurkan</h5>
          </div>
          <div class="column is-6-mobile is-3-desktop has-text-centered">
            <h3 class="title is-1">90%</h3>
            <h5 class="subtitle is-6">Integrasi sistem</h5>
          </div>
          <div class="column is-6-mobile is-3-desktop has-text-centered">
            <h3 class="title is-1">30+</h3>
            <h5 class="subtitle is-6">Partnership</h5>
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
    Cta
  },
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

<style lang="scss">
.home-links a {
  margin-right: 1rem;
}
.lander {
  margin: 0 auto;
  max-width: 400px;
  @media screen and (min-width: 1024px) {
    position: relative;
    &::after {
      content: '';
      background: #eeeeee;
      bottom: -45px;
      right: -170px;
      position: absolute;
      width: 90%;
      height: 90%;
      z-index: 2;
    }
    blockquote {
      position: absolute;
      box-shadow: 60px 40px 60px 0 rgba(19, 23, 32, 0.1);
      max-width: 350px;
      padding: 36px 15px;
      background: #fff;
      bottom: -10px;
      left: -10px;
      z-index: 5;
    }
    img {
      position: relative;
      z-index: 4;
    }
  }
  @media screen and (max-width: 1023px) {
    blockquote {
      display: none;
    }
  }
}
</style>
