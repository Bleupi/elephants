<template>
    <div class="tab-header">
        <ButtonCustom  v-bind:label="label"> {{label}}</ButtonCustom>
    </div>
</template>

<script>
import ButtonCustom from './ButtonCustom.vue';

export default {
  name: 'tab-header',
  props: {
    label: String,
  },
  components: {
    ButtonCustom,
  },
};
</script>

<style>

</style>
