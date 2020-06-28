<template>
  <div class="container flex-column-center">
    <h2>Modul Lengkap untuk Menjalankan Aplikasi PHP Anda.</h2>
    <div class="content-container">
      <div class="column" v-for="(item, idx) in items" :key="idx">
        <p class="row" v-for="(text, i) in item" :key="i">{{ text }}</p>
      </div>
    </div>
    <Button text="Selengkapnya" color="white" />
  </div>
</template>

<script>
  import Button from './Button';

  export default {
    name: 'Modul',
    components: { Button },
    data() {
      return {
        items: [
          [
            'IcePHP',
            'apc',
            'apcu',
            'apm',
            'ares',
            'bcmath',
            'bccompiler',
            'big_int',
            'bitset',
            'bloomy',
            'bz2_filter',
            'clamav',
            'coin_acceptor',
            'crack',
            'dba',
          ],
          [
            'IcePHP',
            'apc',
            'apcu',
            'apm',
            'ares',
            'bcmath',
            'bccompiler',
            'big_int',
            'bitset',
            'bloomy',
            'bz2_filter',
            'clamav',
            'coin_acceptor',
            'crack',
            'dba',
          ],
          [
            'IcePHP',
            'apc',
            'apcu',
            'apm',
            'ares',
            'bcmath',
            'bccompiler',
            'big_int',
            'bitset',
            'bloomy',
            'bz2_filter',
            'clamav',
            'coin_acceptor',
            'crack',
            'dba',
          ],
          [
            'IcePHP',
            'apc',
            'apcu',
            'apm',
            'ares',
            'bcmath',
            'bccompiler',
            'big_int',
            'bitset',
            'bloomy',
            'bz2_filter',
            'clamav',
            'coin_acceptor',
            'crack',
            'dba',
          ],
        ],
      };
    },
  };
</script>

<style lang="scss" scoped>
  .container {
    border-bottom: 1px solid #ccc;
    align-items: center;
    padding: 1.25rem;
  }

  .content-container {
    // background: red;
    width: 90rem;
    display: flex;
    // padding: 0 2.5rem;
    justify-content: center;
    align-items: center;
    margin: 1.25rem 0 2.5rem 0;
  }

  .column {
    width: 15rem;

    .row {
      text-align: center;
    }
  }

  @media (max-width: 48em) {
    h2 {
      text-align: center;
    }

    .content-container {
      flex-direction: column;
    }
  }
</style>
