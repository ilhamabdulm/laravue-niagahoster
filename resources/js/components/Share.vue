<template>
  <div class="container flex-between">
    <p>Bagikan jika Anda menyukai halaman ini</p>
    <div class="social">
      <div class="logo">
        <img :src="icon.fb" alt="fb" />
        <p>80k</p>
      </div>
      <div class="logo">
        <img :src="icon.tw" alt="tw" />
        <p>450</p>
      </div>
      <div class="logo">
        <img :src="icon.google" alt="g+" />
        <p>1900</p>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Share',
    data() {
      return {
        icon: {
          fb: 'images/ic_facebook.svg',
          tw: 'images/ic_twitter.svg',
          google: 'images/ic_google.svg',
        },
      };
    },
  };
</script>

<style lang="scss" scoped>
  .container {
    margin: 0;
    background-color: #f5f5f5;

    p {
      font-size: 1.5rem;
    }
  }

  .social {
    display: flex;

    .logo {
      display: flex;
      align-items: center;
      margin: 0 2rem;
      img {
        margin-right: 0.75rem;
        width: 2.75rem;
        height: 2.75rem;
      }
      p {
        border: 1px solid black;
        padding: 0.5rem 1rem;
      }
    }
  }

  @media (max-width: 48em) {
    .social {
      flex-direction: column;

      .logo {
        display: flex;
        align-items: center;
        margin: 0;
        img {
          width: 2.75rem;
          height: 2.75rem;
        }
        p {
          border: 1px solid black;
          padding: 0.5rem 1rem;
        }
      }
    }
  }
</style>
