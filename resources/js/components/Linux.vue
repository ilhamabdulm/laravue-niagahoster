<template>
  <div class="container flex-column-center">
    <div class="content-container">
      <section>
        <h2>
          Linux Hosting yang Stabil dengan Teknologi LVE
        </h2>
        <p>
          SuperMicro Intel Xeon 24-Cores server dengan RAM 128 GB dan teknologi
          LVE CloudLinux untuk stabilitas server Anda. Dilengkapi dengan SSD
          untuk kecepatan MySQL dan caching. Apache load balancer berbasis
          LiteSpeed Technologies CageFS security Raid-10 protection dan auto
          backup untuk keamanan website PHP Anda.
        </p>
        <Button :text="`Pilih Hosting Anda`" :color="`blue`" />
      </section>
      <section>
        <div class="img-container">
          <img :src="support" alt="support" />
        </div>
      </section>
    </div>
  </div>
</template>

<script>
  import Button from './Button';

  export default {
    name: 'Linux',
    components: { Button },
    data() {
      return {
        support: 'images/grfx_support.png',
      };
    },
  };
</script>

<style lang="scss" scoped>
  .container {
    border-bottom: 1px solid #ccc;
  }

  .content-container {
    display: flex;
    justify-content: space-between;
    margin-bottom: 1.25rem;

    section {
      &:nth-child(1) {
        width: 40%;
        display: flex;
        flex-direction: column;

        h2 {
          font-size: 2.5rem;
          font-weight: 400;
          margin-bottom: 1.25rem;
        }

        p {
          margin: 0;
          font-size: 1.25rem;
          opacity: 0.7;
          margin-bottom: 2.5rem;
        }
      }

      &:nth-child(2) {
        display: flex;
        align-items: flex-end;
      }
    }
  }

  @media (max-width: 48em) {
    .content-container {
      flex-direction: column;
      margin-bottom: 1.25rem;

      section {
        &:nth-child(1) {
          width: 100%;

          h2 {
            font-size: 1.5rem;
            font-weight: 400;
            margin-bottom: 1.25rem;
          }

          p {
            margin: 0;
            font-size: 1rem;
            opacity: 0.7;
            margin-bottom: 2.5rem;
          }
        }

        &:nth-child(2) {
          width: 100%;
          display: flex;
          justify-content: center;
          align-items: flex-end;

          img {
            margin-top: 1.5rem;
            width: 90%;
            height: 90%;
          }
        }
      }
    }
  }
</style>
