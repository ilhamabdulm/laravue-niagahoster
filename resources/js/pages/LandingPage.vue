<template>
  <div>
    <Header />
    <Banner />
    <Content />
    <Modul />
    <Linux />
    <Share />
    <Help />
    <Footer />
  </div>
</template>

<script>
  import Header from '../components/Header';
  import Banner from '../components/Banner';
  import Content from '../components/Content';
  import Modul from '../components/Modul';
  import Linux from '../components/Linux';
  import Share from '../components/Share';
  import Help from '../components/Help';
  import Footer from '../components/Footer';

  export default {
    components: { Header, Banner, Content, Modul, Linux, Share, Help, Footer },
    mounted() {
      console.log('Component mounted.');
    },
  };
</script>

<style lang="scss">
  :root {
    font-size: calc(100vw * 12 / 1440);
  }

  body {
    background-color: #fefefe;
    width: 100%;
  }

  h1 {
    font-size: 3.5rem;
    line-height: 0;
  }

  h2 {
    font-size: 2.5rem;
    font-weight: 400;
  }

  ul {
    padding: 0;
  }

  li {
    list-style: none;
  }

  .container {
    margin: 0 auto;
    padding: 0 7rem;
  }

  .flex-row {
    display: flex;
    justify-content: row;
    align-items: center;
  }

  .flex-between {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .flex-column-center {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .checklist {
    content: '';
    background-color: green;
    width: 1.5rem;
    height: 1.5rem;
    border-radius: 50%;
    margin-right: 0.75rem;

    &::after {
      width: 1.25rem;
      height: 1.25rem;
      display: block;
      border: solid #ffffff;
      border-width: 0 0.2rem 0.2rem 0;
      height: 0.6rem;
      margin: 0.225rem 0 0 0.5rem;
      transform: rotate(45deg);
      width: 0.3rem;
      content: '';
    }
  }

  @media only screen and (max-width: 48em) {
    :root {
      font-size: calc(100vw * 12 / 360);
    }

    .container {
      padding: 0 2rem;
    }

    h1 {
      font-size: 2.5rem;
      line-height: 1;
      margin: 1rem 0 0 0;
    }

    h2 {
      font-size: 1.75rem;
      line-height: 1;
    }

    .flex-between {
      flex-direction: column;
      align-items: flex-start;
    }
  }
</style>
