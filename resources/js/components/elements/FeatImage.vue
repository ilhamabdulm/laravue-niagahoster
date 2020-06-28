<template>
  <div class="feat-image">
    <img :src="image" :alt="name" />
    <p>{{ text }}</p>
  </div>
</template>

<script>
  export default {
    name: 'FeatImage',
    props: ['text', 'name', 'image'],
  };
</script>

<style lang="scss" scoped>
  .feat-image {
    display: flex;
    flex-direction: column;
    align-items: center;
    min-width: 30%;
    img {
      width: 35rem;
      height: 15rem;
      margin-bottom: 1rem;
    }
  }
</style>
