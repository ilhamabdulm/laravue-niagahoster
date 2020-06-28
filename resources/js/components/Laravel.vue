<template>
  <div class="container flex-column-center">
    <h2>Mendukung Penuh Framework Laravel</h2>
    <div class="content-container">
      <section>
        <h5>
          Tak perlu menggunakan dedicated server ataupun VPS yang mahal. Layanan
          PHP hosting murah kami mendukung penuh framework favorit Anda.
        </h5>
        <ul>
          <li>
            <div class="checklist"></div>
            <span>
              Install Laravel <b>1 klik</b> dengan Softculous Installer.
            </span>
          </li>
          <li>
            <div class="checklist"></div>
            <span>
              Mendukung ekstensi <b>PHP MCrypt, phar, mbstring, json</b> dam
              <b>fileinfo</b>.
            </span>
          </li>
          <li>
            <div class="checklist"></div>
            <span>
              Tersedia <b>Composer</b> dan <b>SSH</b> untuk menginstall package
              pilihan Anda
            </span>
            .
          </li>
        </ul>
        <span
          >Nb. Composer dan SSH hanya tersedia pada paket Personal dan
          Bisnis</span
        >
        <Button :text="`Pilih Hosting Anda`" :color="`blue`" />
      </section>
      <section>
        <img :src="laravel" alt="laravel" />
      </section>
    </div>
  </div>
</template>

<script>
  import Button from './Button';

  export default {
    name: 'Laravel',
    components: { Button },
    data() {
      return {
        laravel: 'images/illu_laravel.svg',
      };
    },
  };
</script>

<style lang="scss" scoped>
  .container {
    margin: 0;
  }

  .content-container {
    display: flex;
    justify-content: space-between;

    section {
      &:nth-child(1) {
        width: 50%;
        display: flex;
        flex-direction: column;

        h5 {
          font-size: 2rem;
          font-weight: 400;
          margin-bottom: 1.5rem;
        }

        ul {
          li {
            display: flex;
            font-size: 1.5rem;
            margin: 1rem 0;

            span {
              margin: 0 1.5rem;
            }
          }
        }

        span {
          margin: 1rem 0 2rem 0;
        }
      }

      &:nth-child(2) {
        display: flex;
        align-items: flex-start;

        img {
          width: 40rem;
          height: 40rem;
        }
      }
    }
  }

  @media (max-width: 48em) {
    .container {
      h2 {
        text-align: center;
      }
    }

    .content-container {
      flex-direction: column;

      section {
        &:nth-child(1) {
          width: 100%;
          margin-bottom: 2rem;

          h5 {
            font-size: 1.5rem;
            font-weight: 400;
            margin-bottom: 1.5rem;
          }

          ul {
            li {
              display: flex;
              font-size: 0.85rem;
              margin: 1rem 0;

              span {
                margin: 0 1rem;
              }
            }
          }

          span {
            font-size: 0.75rem;
            margin: 1rem 0 2rem 0;
          }
        }

        &:nth-child(2) {
          margin-top: 2rem;
          img {
            width: 100%;
            height: 100%;
          }
        }
      }
    }
  }
</style>
