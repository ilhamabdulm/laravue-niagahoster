<template>
  <div class="container">
    <div class="content flex-between">
      <p>Perlu <b>BANTUAN?</b> Hubungi Kami : <b>0274-5305505</b></p>
      <button>
        <img :src="talk" alt="live" />
        <span>Live Chat</span>
      </button>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Help',
    data() {
      return {
        talk: 'images/ic_talk.svg',
      };
    },
  };
</script>

<style lang="scss" scoped>
  .container {
    margin: 0;
    background-color: #298eea;

    .content {
      padding: 4rem 0;
      p {
        font-size: 2.25rem;
        color: #fefefe;
      }
    }
  }

  button {
    border: 1.5px solid #fefefe;
    padding: 1rem 2.5rem;
    background: transparent;
    display: flex;
    align-items: center;
    border-radius: 5rem;
    width: 15rem;
    cursor: pointer;

    span {
      color: #fefefe;
      font-size: 1.25rem;
      margin: 0 1.25rem;
    }

    &:hover {
      background-color: #0764b6;
      border: none;
    }

    img {
      widows: 2rem;
      height: 2rem;
    }
  }

  @media (max-width: 48em) {
    .container {
      .content {
        p {
          font-size: 1.75rem;
          color: #fefefe;
        }
      }
    }
  }
</style>
