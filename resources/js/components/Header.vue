<template>
  <header>
    <div class="contact-info">
      <div class="container flex-between">
        <div class="flex-row">
          <img :src="icon.bookmark" alt="book" class="icon-mini" />
          <p>Gratis Ebook 9 Cara Cerdas Menggunakan Domain[x]</p>
        </div>
        <div>
          <span class="flex-row">
            <img :src="icon.phone" alt="phone" class="icon-mini" />
            <p>0274-5305505</p>
          </span>
          <span class="flex-row">
            <img :src="icon.talk" alt="chat" class="icon-mini" />
            <p>Live Chat</p>
          </span>
          <span class="flex-row">
            <img :src="icon.account" alt="account" class="icon-mini" />
            <p>Member Area</p>
          </span>
        </div>
      </div>
    </div>
    <div class="main">
      <div class="container flex-between">
        <div class="icon">
          <img :src="logo" alt="logo" />
        </div>
        <nav>
          <a href="#">Hosting</a>
          <a href="#">Domain</a>
          <a href="#">Server</a>
          <a href="#">Website</a>
          <a href="#">Afiliasi</a>
          <a href="#">Promo</a>
          <a href="#">Pembayaran</a>
          <a href="#">Review</a>
          <a href="#">Kontak</a>
          <a href="#">Blog</a>
        </nav>
      </div>
    </div>
  </header>
</template>

<script>
  export default {
    name: 'Header',
    data() {
      return {
        logo: 'images/grfx_logo.png',
        icon: {
          phone: 'images/ic_phone.svg',
          talk: 'images/ic_talk.svg',
          account: 'images/ic_account.svg',
          bookmark: 'images/ic_bookmark.svg',
        },
      };
    },
    mounted() {
      console.log('Component Mounted');
    },
  };
</script>

<style lang="scss" scoped>
  @import '../../sass/variables';

  header {
    position: sticky;
    top: 0;
    z-index: 10000;
    background: #fefefe;
  }

  .contact-info {
    padding: 0.5rem 0;
    border-bottom: 1px solid #ccc;
  }

  .contact-info > .container > div {
    display: flex;
    justify-content: space-between;
    width: 22.5%;
  }

  .main {
    padding: 1.25rem 0;
    border-bottom: 1px solid #ccc;
  }

  .icon {
    width: 25%;
    font-size: 2.5rem;

    img {
      width: 17.5rem;
      height: 5rem;
    }
  }

  .icon-mini {
    width: 1.25rem;
    height: 1.25rem;
    margin-right: 0.25rem;
  }

  .main {
    .container {
      nav {
        width: 75%;
        display: flex;
        justify-content: space-between;
        a {
          font-size: 1.5rem;
          text-decoration: none;
          color: #000;
          cursor: pointer !important;
        }
      }
    }
  }

  @media (max-width: 48em) {
    .contact-info {
      display: none;
    }

    .main {
      .container {
        nav {
          display: none;
        }
      }
    }
  }
</style>
