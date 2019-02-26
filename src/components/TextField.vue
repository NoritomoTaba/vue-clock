<template>
  <input
    type="text"
    class="TextField"
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
.TextField {
  min-width: 15rem;
  border: 2rem border #444444;
  margin-right: 1rem;
  padding: 1rem .5rem 1rem;
  style: inline-block;
}
</style>
