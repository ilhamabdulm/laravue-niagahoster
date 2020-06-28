<template>
  <button :class="color">{{ text }}</button>
</template>

<script>
  export default {
    name: 'Button',
    props: ['color', 'text'],
  };
</script>

<style lang="scss" scoped>
  button {
    padding: 0.75rem 1.5rem;
    font-size: 1.25rem;
    font-weight: 600;
    border: none;
    max-width: 15rem;
    border-radius: 5rem;
    cursor: pointer;

    &.white {
      color: #2b2c2c;
      background-color: #fefefe;
      border: 1px solid #2b2c2c;

      &:hover {
        background-color: #fafafa;
      }
    }

    &.blue {
      color: #fefefe;
      background-color: #298eea;
      border: 1px solid #298eea;

      &:hover {
        background-color: #0764b6;
      }
    }
  }
</style>
