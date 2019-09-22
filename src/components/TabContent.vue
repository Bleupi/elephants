<template>
    <div class="tab-content">
        <img  v-bind:src="image"/>
        <div class="name"> {{ name }} </div>
        <div class="description"> {{ description }}</div>
        <router-link  v-bind:to="link" class="link"> Discover more on wikipedia </router-link>
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
