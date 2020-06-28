<template>
  <div class="container flex-column-center">
    <h2>Semua Paket Hosting Sudah Termasuk</h2>
    <div class="card-container">
      <HostImage
        v-for="(hosting, i) in hostingList"
        :key="i"
        :image="hosting.image"
        :title="hosting.text"
        :caption="hosting.caption"
        :name="hosting.name"
      />
    </div>
  </div>
</template>

<script>
  import HostImage from './elements/HostImage';

  export default {
    name: 'Hosting',
    components: { HostImage },
    data() {
      return {
        hostingList: [
          {
            image: 'images/ic_allversion.svg',
            text: 'PHP Semua Versi',
            caption:
              'Pilih mulai dari versi PHP 5.3 s/d PHP 7. Ubah sesuka Anda!',
            name: 'php',
          },
          {
            image: 'images/ic_mysql.svg',
            text: 'MySQL Versi 5.6',
            caption:
              'Nikmati MySQL versi terbari, tercepat, dan kaya akan fitur.',
            name: 'mysql',
          },
          {
            image: 'images/ic_cpanel.svg',
            text: 'Panel Hosting cPanel',
            caption:
              'Kelola website dengan panel canggih yang familiar di hati Anda.',
            name: 'cpanel',
          },
          {
            image: 'images/ic_garansi.svg',
            text: 'Garansi Uptime 99.9%',
            caption:
              'Data center yang mendukung kelangsungan website Anda 24/7',
            name: 'garansi',
          },
          {
            image: 'images/ic_unlimited.svg',
            text: 'Database InnoDB Unlimited',
            caption:
              'Jumlah dan ukuran database yang tumbuh sesuai kebutuhan Anda.',
            name: 'unlimited',
          },
          {
            image: 'images/ic_remote.svg',
            text: 'Wildcard Remote MySQL',
            caption:
              'Mendukung s/d 25 max_user_connections dari 100 max_connections',
            name: 'remote',
          },
        ],
      };
    },
  };
</script>

<style lang="scss" scoped>
  .card-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }

  @media (max-width: 48em) {
    .container {
      h2 {
        text-align: center;
      }

      .card-container {
        flex-direction: column;
      }
    }
  }
</style>
