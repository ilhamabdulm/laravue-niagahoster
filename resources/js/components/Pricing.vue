<template>
  <div class="container">
    <div class="title">
      <h1>Paket Hosting Singapura yang Tepat</h1>
      <h3>Diskon 40% + Domain dan SSL Gratis untuk Anda</h3>
    </div>
    <main>
      <div class="card">
        <div class="card-title">Bayi</div>
        <div class="card-price">
          <span>{{ pricings['bayi']['old_price'] }}</span>
          <h3>{{ pricings['bayi']['new_price'] }}<span>/bln</span></h3>
        </div>
        <div class="card-user"><b>939</b> Pengguna Terdaftar</div>
        <div class="card-body">
          <p>0.5X RESOURCE POWER</p>
          <p>500MB Disk Space</p>
          <p>Unlimited Bandwitch</p>
          <p>Unlimited Database</p>
          <p>1 Domain</p>
          <p>Instant Backup</p>
          <p>Unlimited SSL Gratis Selamanya</p>
        </div>
        <div class="card-action">
          <Button text="Pilih Sekarang" color="white" />
        </div>
      </div>
      <div class="card">
        <div class="card-title">Pelajar</div>
        <div class="card-price">
          <span>{{ pricings['pelajar']['old_price'] }}</span>
          <h3>{{ pricings['pelajar']['new_price'] }}<span>/bln</span></h3>
        </div>
        <div class="card-user"><b>939</b> Pengguna Terdaftar</div>
        <div class="card-body">
          <p>0.5X RESOURCE POWER</p>
          <p>500MB Disk Space</p>
          <p>Unlimited Bandwitch</p>
          <p>Unlimited Database</p>
          <p>1 Domain</p>
          <p>Instant Backup</p>
          <p>Unlimited SSL Gratis Selamanya</p>
          <p>Unlimited SSL Gratis Selamanya</p>
        </div>
        <div class="card-action">
          <Button text="Pilih Sekarang" color="white" />
        </div>
      </div>
      <div class="card active">
        <div class="ribbon">
          <span>BEST SELLER</span>
        </div>
        <div class="card-title">Personal</div>
        <div class="card-price">
          <span>{{ pricings['personal']['old_price'] }}</span>
          <h3>{{ pricings['personal']['new_price'] }}<span>/bln</span></h3>
        </div>
        <div class="card-user"><b>939</b> Pengguna Terdaftar</div>
        <div class="card-body">
          <p>0.5X RESOURCE POWER</p>
          <p>500MB Disk Space</p>
          <p>Unlimited Bandwitch</p>
          <p>Unlimited Database</p>
          <p>1 Domain</p>
          <p>Instant Backup</p>
          <p>Unlimited SSL Gratis Selamanya</p>
          <p>Instant Backup</p>
          <p>Unlimited SSL Gratis Selamanya</p>
        </div>
        <div class="card-action">
          <Button text="Pilih Sekarang" color="blue" />
        </div>
      </div>
      <div class="card">
        <div class="card-title">Bisnis</div>
        <div class="card-price">
          <span>{{ pricings['bisnis']['old_price'] }}</span>
          <h3>{{ pricings['bisnis']['new_price'] }}<span>/bln</span></h3>
        </div>
        <div class="card-user"><b>939</b> Pengguna Terdaftar</div>
        <div class="card-body">
          <p>0.5X RESOURCE POWER</p>
          <p>500MB Disk Space</p>
          <p>Unlimited Bandwitch</p>
          <p>Unlimited Database</p>
          <p>1 Domain</p>
          <p>Instant Backup</p>
          <p>Unlimited SSL Gratis Selamanya</p>
          <p>Instant Backup</p>
          <p>Unlimited SSL Gratis Selamanya</p>
          <p>Instant Backup</p>
          <p>Unlimited SSL Gratis Selamanya</p>
        </div>
        <div class="card-action">
          <Button text="Pilih Sekarang" color="white" />
        </div>
      </div>
    </main>
  </div>
</template>

<script>
  import Button from './Button';
  import axios from 'axios';
  export default {
    name: 'Pricing',
    components: { Button },
    data() {
      return {
        pricings: {},
      };
    },
    mounted() {
      axios.get('/api/pricing').then((res) => {
        this.pricings = res.data;
      });
    },
  };
</script>

<style lang="scss" scoped>
  main {
    display: flex;
    justify-content: center;
    align-items: flex-start;
  }

  .title {
    text-align: center;
    padding: 2.5rem 0;

    h1 {
      font-size: 2.5rem;
    }

    h3 {
      font-size: 2.25rem;
      font-weight: 200;
    }
  }

  .card {
    border: 1px solid #ccc;
    margin: 0 0.25rem;
    min-width: 22.5%;
    height: auto;

    &.active {
      position: relative;
      .card-title,
      .card-price {
        background-color: #298eea;
        color: #fefefe;
      }

      .card-user {
        background-color: #0764b6;
        color: #fefefe;
      }

      .ribbon {
        display: block;
        content: '';
        height: 10rem;
        width: 10rem;
        position: absolute;
        top: -0.5rem;
        left: -0.5rem;
        overflow: hidden;

        span {
          position: absolute;
          width: 13rem;
          padding: 1rem;
          font-weight: 600;
          font-size: 1.25rem;
          color: #fefefe;
          text-align: center;
          background-color: #71dd51;
          transform: rotate(-45deg);
          top: 2rem;
          left: -3.5rem;
          box-shadow: 2px 2px 2px #2b2c2c;
        }
      }
    }

    .ribbon {
      display: none;
    }

    .card-title {
      font-size: 2rem;
      font-weight: 600;
      padding: 0.5rem 0;
      text-align: center;
      border-bottom: 1px solid #ccc;
    }

    .card-price {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 0.5rem 0;
      border-bottom: 1px solid #ccc;

      & > span {
        text-decoration: line-through;
        font-size: 1.25rem;
      }

      h3 {
        font-size: 2rem;

        & > span {
          font-size: 1rem;
        }
      }
    }

    .card-user {
      padding: 0.75rem 0;
      border-bottom: 1px solid #ccc;
      text-align: center;
    }

    .card-body {
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    .card-action {
      text-align: center;
      margin: 2.5rem 0 1.5rem 0;
    }
  }

  @media (max-width: 48em) {
    main {
      flex-direction: column;
      align-items: center;
    }

    .card {
      width: 100%;
      margin-bottom: 1.5rem;
    }
  }
</style>
