<template>
  <p>{{ message }}</p>
</template>

<script>
import Vue from "vue";

export default Vue.extend({
  name: "Print",
  props: {
    message: {
      type: String,
    },
  },
});
</script>

<style>
</style>
