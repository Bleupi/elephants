<template>
    <div class="tabs">
        <div class="tabs-header">
        <TabHeader
            v-for="tab in tabs"
            v-bind:key="tab._id"
            v-bind:label="tab.name"
            v-bind:tab="tab"
        > </TabHeader>
        </div>
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
.tabs-header {
    display: flex;
    flex-direction: row;
    overflow: hidden;
    border: 1px solid #ccc;
    background-color: #f1f1f1;
    justify-content: space-between;
}
.tabs-content { 
    display: none;
    padding: 6px 12px;
    border: 1px solid #ccc;
    border-top: none;
}
</style>
