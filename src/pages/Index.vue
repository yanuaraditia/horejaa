<template>
  <Layout>
    <section class="section zed">
      <div class="container is-fluid">
        <div class="columns">
          <div class="column is-6-desktop">
            <h1 class="title is-1 is-4-mobile">Mudah, efisien, <br>dan tepat waktu</h1>
            <p class="font-primary" style="margin-bottom: 10px">Palagan Food Supplier, kami adalah supplier yang bergerak di bidang bahan pokok pangan khususnya untuk hotel, restoran, dan kafe. Demi menunjang kemudahan dan kelancaran bisnis usaha anda, kami menghadirkan sebuah aplikasi yang bernama Horekaa. </p>
            <p class="font-primary" style="margin-bottom: 20px">Horeka memiliki tujuan untuk mempermudah pemesanan bahan bahan baku kebutuhan bisnis anda serta melakukan pencegahan terhadap kelalaian untuk melakukan pemesanan bahan yang sering terjadi di industri ini.</p>
            <p class="home-links">
              <a href="mailto:kharisma.fr@gmail.com" class="button is-primary is-medium is-rounded">Yuk Cobain</a>
              <!-- <g-link to="/register" class="button is-primary is-medium is-rounded">Coba Sekarang</g-link> -->
            </p>
            <hr>
            <ul class="list-group">
              <li>Mudahnya memesan barang</li>
              <li>Rekapan transaksi (pembelian dan pemesanan barang)</li>
              <li>Rekapan penggunaan bahan baku</li>
            </ul>
          </div>
          <div class="column is-6-desktop">
            <div class="lander">
              <span class="dotted-box"></span>
              <g-image src="~/images/banner-front.jpg" class="rad-5" width="400px" blur="3" radius="3"></g-image>
              <blockquote>
                <p>"Kami telah melihat penghematan biaya 25,3% sejak beralih ke Horekaa, karena kami menggunakan tiga pusat pemenuhan mereka."</p>
                <img src="/quote.svg" alt="Quote">
              </blockquote>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="section zed">
      <div class="container is-fluid">
        <div class="columns is-multiline is-flex">
          <div class="column is-6-mobile is-4-desktop has-text-centered">
            <h3 class="title is-1">99.91%</h3>
            <h5 class="subtitle is-6">Akurasi tinggi</h5>
          </div>
          <div class="column is-6-mobile is-4-desktop has-text-centered">
            <h3 class="title is-1">3.500+</h3>
            <h5 class="subtitle is-6">Produk telah tersalurkan</h5>
          </div>
          <div class="column is-6-mobile is-4-desktop has-text-centered">
            <h3 class="title is-1">35+</h3>
            <h5 class="subtitle is-6">Outlet Partnership</h5>
          </div>
        </div>
      </div>
    </section>
    <section class="warehouse section zed mar">
      <div class="container is-fluid">
        <div class="columns">
          <div class="column is-12-mobile is-6-desktop has-text-centered">
            <div class="lunar" style="max-width: 400px; margin: 0 auto;">
              <span class="dotted-box"></span>
              <g-image src="~/images/warehouse.jpg" width="400px" blur="3" class="rad-5"></g-image>
            </div>
          </div>
          <div class="column is-12-mobile is-6-desktop">
            <div class="lunar-x" style="max-width: 500px">
              <h2 class="title is-1">Jaringan pusat pemenuhan yang kuat</h2>
              <p>Kami membantu Anda menentukan penempatan inventaris yang optimal di seluruh jaringan pemenuhan yang berkembang untuk meningkatkan kecepatan pengiriman dan mengurangi biaya pengiriman. Anda dapat mengukur secara efisien dengan mendistribusikan inventaris ke gudang tambahan seiring waktu.</p>
              <ul class="list-group">
                <li>Sistem kami dapat mempermudah anda dalam memantau stok bahan baku</li>
                <li>Gratis layanan pengiriman dengan jaminan tepat waktu</li>
                <li>Katalog barang yang lengkap, bahkan anda dapat melakukan request barang</li>
              </ul>
              <hr/>
              <small>Kami mengirim ke mana saja di dunia yang dikirimkan oleh operator.</small>
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
  position: relative;
  .dotted-box {
    position: absolute;
    z-index: 4;
    right: 0;
    @media screen and (min-width: 1024px) {
      transform: translateY(-30px) translateX(30px);
    }
  }
  @media screen and (min-width: 1024px) {
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
  }
  img {
    position: relative;
    z-index: 4;
  }
  @media screen and (max-width: 1023px) {
    blockquote {
      display: none;
    }
  }
  blockquote {
    img {
      position: absolute;
      top: -10px;
      left: -20px;
    }
  }
}
.lunar {
  position: relative;
  .dotted-box {
    position: absolute;
    $offset: -30px;
    transform: translateX($offset) translateY($offset);
    z-index: 4;
  }
  img {
    position: relative;
    z-index: 5;
  }
}
</style>
