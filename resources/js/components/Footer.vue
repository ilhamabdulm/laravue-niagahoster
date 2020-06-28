<template>
  <footer>
    <div class="container">
      <div class="row">
        <div class="col">
          <h3>Hubungi Kami</h3>
          <p>0274-5305505</p>
          <p>Senin - Minggu</p>
          <p class="spacer">24 Jam Nonstop</p>
          <p>Jl. Selokan Mataram Monjali</p>
          <p>Karangjati MT I/304</p>
          <p>Sinduadi, Mlati, Sleman</p>
          <p>Yogyakarta 55284</p>
        </div>
        <div class="col">
          <h3>Layanan</h3>
          <p>Domain</p>
          <p>Shared Hosting</p>
          <p>Cloud VPS Hosting</p>
          <p>Managed BPS Hosting</p>
          <p>Web Builder</p>
          <p>Keamanan SSL / HTTPS</p>
          <p>Jasa Pembuatan Website</p>
          <p>Program Afiliasi</p>
        </div>
        <div class="col">
          <h3>Service Hosting</h3>
          <p>Hosting Murah</p>
          <p>Hosting Indonesia</p>
          <p>Hosting Singapura SG</p>
          <p>Hosting PHP</p>
          <p>Hosting Wordpress</p>
          <p>Hosting Laravel</p>
        </div>
        <div class="col">
          <h3>Tutorial</h3>
          <p>Knowledgebase</p>
          <p>Blog</p>
          <p>Cara Pembayaran</p>
        </div>
      </div>
      <div class="row">
        <div class="col">
          <h3>Tentang Kami</h3>
          <p>Tim Niagahoster</p>
          <p>Karir</p>
          <p>Events</p>
          <p>Penawaran & Promo Spesial</p>
          <p>Kontak Kami</p>
        </div>
        <div class="col">
          <h3>Kenapa Pilih Niagahoster?</h3>
          <p>Support Terbaik</p>
          <p>Garansi Harga Terbaik</p>
          <p>Domain Gratis Selamanya</p>
          <p>Datacenter Hosting Terbaik</p>
          <p>Review Pelanggan</p>
        </div>
        <div class="col">
          <h3>Newsletter</h3>
          <label>
            <input
              type="email"
              name="subs"
              class="input-field"
              placeholder="Email"
            />
            <Button text="Berlangganan" color="blue" class="subs-btn">
              Browse
            </Button>
          </label>
          <span
            >Dapatkan promo dan konten menarik dari penyedia hosting terbaik
            Anda.</span
          >
        </div>
        <div class="col image">
          <img :src="images.socmed" alt="socmed" />
        </div>
      </div>
      <div class="row">
        <div class="col">
          <h3>Pembayaran</h3>
          <img :src="images.payment" alt="payment" class="long-img" />
          <span
            >Aktivasi instan dengan e-Payment. Hosting dan domain langsung
            aktif!</span
          >
        </div>
      </div>
      <section>
        <div class="copyright">
          <p>
            Copyright &copy; Niagahoster | Hosting powered by PHP7, CloudLinux,
            CloudFlare, BitNinja, and DC Biznet Technovillage Jakarta
          </p>
          <p>Syarat dan Ketentuan | Kebijakan Privasi</p>
        </div>
        <p>
          Cloud VPS Murah powered by Webuzo Softculous, Intel SSD, and cloud
          computing technology
        </p>
      </section>
    </div>
  </footer>
</template>

<script>
  import Button from './Button';

  export default {
    name: 'Footer',
    components: { Button },
    data() {
      return {
        images: {
          payment: 'images/grfx_payment.png',
          socmed: 'images/grfx_socmed.png',
        },
      };
    },
  };
</script>

<style lang="scss" scoped>
  footer {
    padding: 1rem 0;
    background-color: #303030;
    color: #fefefe;

    h3 {
      font-size: 1.35rem;
      color: #8e8e8e;
      margin-bottom: 1.5rem;
      text-transform: uppercase;
    }
  }

  label {
    position: relative;

    .input-field {
      padding: 1.25rem 6rem 1.25rem 2rem;
      font-size: 1.25rem;
      border-radius: 3rem;
      width: 70%;
      margin-bottom: 1.25rem;
    }

    .subs-btn {
      position: absolute;
      left: 13rem;
      top: -1rem;
    }
  }

  .row {
    display: flex;
    margin-bottom: 4rem;

    .col {
      width: 25%;

      .spacer {
        margin-bottom: 3rem;
      }

      span {
        color: #8e8e8e;
      }

      &.image {
        display: flex;
        align-items: flex-start;
        padding: 4.25rem 1.25rem;
        margin-left: 2rem;
      }

      img {
        margin-bottom: 1.5rem;
      }
    }
  }

  .container {
    section {
      display: flex;
      flex-direction: column;

      & > p {
        color: #fefefe;
        margin-top: 0;
      }

      .copyright {
        display: flex;
        justify-content: space-between;

        p {
          color: #fefefe;
        }
      }
    }
  }

  @media (max-width: 48em) {
    .row {
      flex-direction: column;

      .col {
        width: 100%;

        &.image {
          display: flex;
          align-items: flex-start;
          padding: 4.25rem 1.25rem;
          margin-left: 2rem;
        }

        img {
          margin-bottom: 1.5rem;
        }
      }
    }

    .long-img {
      width: 100%;
    }

    .copyright {
      flex-direction: column;
    }
  }
</style>
