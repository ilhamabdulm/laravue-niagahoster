<template>
  <main>
    <div class="container flex-between">
      <section id="left">
        <h1>PHP Hosting</h1>
        <h2>Cepat, handal, penuh dengan modul PHP yang Anda butuhkan</h2>
        <ul>
          <li>
            <div class="checklist"></div>
            Solusi PHP untuk performa query yang lebih cepat
          </li>
          <li>
            <div class="checklist"></div>
            Konsumsi memori yang lebih rendah
          </li>
          <li>
            <div class="checklist"></div>
            Support PHP 5.3, PHP 5.4, PHP 5.5, PHP 5.6, dan PHP 7
          </li>
          <li>
            <div class="checklist"></div>
            Fitur enkripsi IonCube dan Zend Guard Loaders
          </li>
        </ul>
      </section>
      <section id="right">
        <img :src="image" alt="banner-img" />
      </section>
    </div>
  </main>
</template>

<script>
  export default {
    name: 'Banner',
    data() {
      return { image: 'images/illu_banner.svg' };
    },
  };
</script>

<style lang="scss" scoped>
  main {
    border-bottom: 1px solid #ccc;
    height: auto;
    display: flex;
  }

  #left {
    width: 40%;
    h2 {
      font-weight: 400;
    }
    ul {
      padding: 0;
      li {
        display: flex;
        align-items: center;
        margin: 0.75rem 0;
      }
    }
  }

  #right {
    img {
      width: 42.5rem;
      height: 42.5rem;
    }
  }

  @media (max-width: 48em) {
    #left,
    #right {
      width: 100%;
    }

    #right {
      img {
        width: 100%;
        height: 100%;
      }
    }
  }
</style>
