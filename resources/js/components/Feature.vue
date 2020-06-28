<template>
  <section>
    <div class="container flex-center">
      <div v-for="(image, i) in images" :key="i">
        <FeatImage :text="image.text" :image="image.image" :name="image.name" />
      </div>
    </div>
  </section>
</template>

<script>
  import FeatImage from './elements/FeatImage';

  export default {
    name: 'Feature',
    components: { FeatImage },
    data() {
      return {
        images: [
          {
            text: 'PHP Zen Guard Loaded',
            image: 'images/illu_zenguard.svg',
            name: 'zen',
          },
          {
            text: 'PHP Composer',
            image: 'images/illu_composer.svg',
            name: 'comp',
          },
          {
            text: 'PHP IonCube Loader',
            image: 'images/illu_ioncube.svg',
            name: 'ion',
          },
        ],
      };
    },
  };
</script>

<style lang="scss" scoped>
  .flex-center {
    display: flex;
    justify-content: space-around;
  }

  @media (max-width: 48em) {
    .flex-center {
      flex-direction: column;
    }
  }
</style>
