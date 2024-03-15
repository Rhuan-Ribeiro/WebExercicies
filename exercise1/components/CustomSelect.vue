<script lang="ts" setup>
const props = defineProps({
  text: {type: String, required: true},
  options: {type: Object, required: true},
  value: {type: String, require: true}
});

const select = defineModel();
</script>

<template>
  <div>
    <select v-model="select">
      <option v-for="option in props.options" v-bind:value="option.value">
        {{ option.text }}
      </option>
    </select>
  </div>
</template>

<style>

</style>