<template>
  <input
    type="text"
    class="country"
    :value="value"
    v-on:input="onInput"
  />
</template>

<script>
import Vue from "Vue";

export default {
  props: {
    value: {
      type: String,
    },
  },
};
</script>

<style scoped>
.country {
  min-width: 300px;
  border: 1px solid #444444;
  padding: 17px 25px;
}
</style>
