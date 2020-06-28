<template>
  <section class="limit">
    <div class="container flex-column-center">
      <h2>Powerful dengan Limit PHP yang lebih besar</h2>
      <div class="box-container">
        <div class="box">
          <div class="row">
            <div class="checklist"></div>
            <p>max execution time 300s</p>
          </div>
          <div class="row">
            <div class="checklist"></div>
            <p>max execution time 300s</p>
          </div>
          <div class="row">
            <div class="checklist"></div>
            <p>php memory limit 1024 MB</p>
          </div>
        </div>
        <div class="box">
          <div class="row">
            <div class="checklist"></div>
            <p>post max size 128 MB</p>
          </div>
          <div class="row">
            <div class="checklist"></div>
            <p>upload max filesize 128 MB</p>
          </div>
          <div class="row">
            <div class="checklist"></div>
            <p>max input vars 2500</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
  export default {
    name: 'Limit',
  };
</script>

<style lang="scss" scoped>
  section {
    padding: 1.25rem 0;
    .container {
      h2 {
        font-weight: 400;
      }
    }
  }

  .box-container {
    display: flex;
  }

  .box {
    display: flex;
    flex-direction: column;
    margin: 0 1.5rem;

    .row {
      padding: 0.5rem 1.25rem;
      width: 30rem;
      display: flex;
      align-items: center;
      border: 0.5px solid #ccc;

      p {
        margin: 1.5rem auto;
        font-size: 1.25rem;
      }

      &:nth-child(2) {
        background-color: #f5f5f5;
      }
    }
  }

  @media (max-width: 48em) {
    .container {
      h2 {
        text-align: center;
      }
    }

    .box-container {
      flex-direction: column;
    }

    .box {
      margin: 1.5rem 0;
      .row {
        width: 100%;
      }
    }
  }
</style>
