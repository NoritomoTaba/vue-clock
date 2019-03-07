<template>
    <input
      type="text"
      placeholder="hogehoge"
      class="TextField"
      v-on:input="onInput"
    />
</template>

<script>
import Vue from "vue";

export default Vue.extend({
  name: "TextField",
  methods: {
    onInput() {
      this.$emit("input",value);
    },
  },
});
</script>

<style scoped>
.TextField input {
  min-width: 15rem;
  text-transform: uppercase;
  border: 2rem border #444444;
  margin-right: 1rem;
  padding: 1rem .5rem 1rem;
  style: inline-block;
}
</style>
