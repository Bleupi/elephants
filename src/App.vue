<template>
  <div id="app">
    <div>
      Elephants
    </div>
    <div v-if="loading" class="loading">
      Loading...
    </div>
    <div v-if="error" class="error">
      {{ error }}
    </div>
    <Tabs
      v-bind:tabs="tabs"
    > </Tabs>
  </div>
</template>

<script>
import Tabs from './components/Tabs.vue';
import elephants from './tmp.json';

export default {
  name: 'app',
  components: {
    Tabs,
  },
  data() {
    return {
      loading: false,
      tabs: elephants.elephants,
      error: null,
    };
  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
