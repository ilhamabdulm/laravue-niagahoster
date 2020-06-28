<template>
  <div class="root">
    <img :src="image" :alt="name" />
    <h3>{{ title }}</h3>
    <p>{{ caption }}</p>
  </div>
</template>

<script>
  export default {
    name: 'HostImage',
    props: ['image', 'title', 'caption', 'name'],
  };
</script>

<style lang="scss" scoped>
  .root {
    min-width: 25%;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 1.25rem 2rem;

    h3 {
      font-weight: 600;
      font-size: 1.25rem;
      margin: 0.25rem 0;
    }

    p {
      font-size: 1rem;
      width: 80%;
      text-align: center;
    }

    img {
      width: 5rem;
      height: 5rem;
      margin-bottom: 1.5rem;
    }
  }
</style>
