<template>
  <button> {{label}} </button>
</template>

<script>
export default {
  name: 'button-custom',
  props: {
    label: String,
    action: String,
  },
};
</script>

<style>

</style>
