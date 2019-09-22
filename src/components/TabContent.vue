<template>
    <div class="tab-content">
        <img  v-bind:src="image"/>
        <div tab-subcontent>
            <h3 class="name"> {{ name }} </h3>
            <div class="description"> {{ description }}</div>
            <a v-bind:href="link" class="link"> Discover more on wikipedia </a>
        </div>
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
.tab-content {
    display:flex;
    
}
img {
    border-radius: 50%
}
.name {
    font-weight: bold
}
</style>
