<template>
  <div class="page">
    <Feature />
    <Pricing />
    <Limit />
    <Hosting />
    <Laravel />
  </div>
</template>

<script>
  import Feature from './Feature';
  import Pricing from './Pricing';
  import Limit from './Limit';
  import Hosting from './Hosting';
  import Laravel from './Laravel';

  export default {
    name: 'Content',
    components: { Feature, Pricing, Limit, Hosting, Laravel },
  };
</script>

<style lang="scss" scoped>
  .page {
    border-bottom: 1px solid #ccc;
    margin: 1.25rem 0;
    padding: 1rem 0;

    * {
      margin: 1.25rem 0;
    }
  }
</style>
