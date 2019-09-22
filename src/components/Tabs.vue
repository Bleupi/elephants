<template>
    <div class="tabs">
        <TabHeader
            v-for="tab in tabs"
            v-bind:key="tab._id"
            v-bind:label="tab.name"
            v-bind:tab="tab"
        > </TabHeader>
      <div class="tabs-content">
        <div>
          content tab1      
        </div>
        <div>
          content tab2      
        </div>
        <div>
          content tab3
        </div>
      </div>
    </div>
</template>

<script>
import TabHeader from './TabHeader.vue'

export default {
  name:'tabs',
  props: {
    tabs: Array,
  },
  components: {
    TabHeader,
  }
  
}
</script>

<style>

</style>
