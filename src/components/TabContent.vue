<template>
    <div class="tab-content">
        <img  v-bind:src="image"/>
        <div class="name"> {{ name }} </div>
        <div class="description"> {{ description }}</div>
        <a v-bind:href="link" class="link"> Discover more on wikipedia </a>
    </div>
</template>

<script>
export default {
  name: 'tab-content',
  props: {
    name: String,
    description: String,
    link: String,
    image: String,
  },
};
</script>

<style>

</style>
