<template>
    <div v-bind:class="{'tab-header': true, active: selected }">
        <h2>
        <ButtonCustom  v-bind:label="label"> {{label}}</ButtonCustom>
        </h2>
    </div>
</template>

<script>
import ButtonCustom from './ButtonCustom.vue';

export default {
  name: 'tab-header',
  props: {
    label: String,
    selected: Boolean,
  },
  components: {
    ButtonCustom,
  },
};
</script>

<style>
.tab-header {
    background-color: inherit;
    float: left;
    border: none;
    outline: none;
    cursor: pointer;
    padding: 14px 16px;
    transition: 0.3s;
}
.tab-header:hover {
    background-color: #ddd;
}
.tab-header.active {
    background-color: #ccc;
}
</style>
