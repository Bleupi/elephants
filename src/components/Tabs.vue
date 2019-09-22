<template>
    <div class="tabs">
        <TabHeader
            v-for="tab in tabs"
            v-bind:key="tab._id"
            v-bind:label="tab.name"
            v-bind:tab="tab"
        > </TabHeader>
      <div class="tabs-content">
        <TabContent
            v-for="tab in tabs"
            v-bind:key="tab._id"
            v-bind:name="tab.name"
            v-bind:description="tab.note"
            v-bind:link="tab.wikilink"
            v-bind:image="tab.image"
        >
        </TabContent>
      </div>
    </div>
</template>

<script>
import TabHeader from './TabHeader.vue';
import TabContent from './TabContent.vue';

export default {
  name: 'tabs',
  props: {
    tabs: Array,
  },
  components: {
    TabHeader,
    TabContent,
  },

};
</script>

<style>

</style>
