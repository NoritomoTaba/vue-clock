<template>
  <div class="TextField">
    <input
      type="text"
      v-bind:text="text"
      v-on:input="onInput"
      placeholder="都市名を入力してください"
    />
  </div>
</template>

<script>
import Vue from "vue";

export default Vue.extend({
  name: "TextField",
  props: {
    text: {
      type: String,
    },
  },
  methods: {
    onInput() {
      this.$emit("input",text);
    },
  },
});
</script>

<style scoped>
.TextField input{
  min-width: 15rem;
  text-transform: uppercase;
  border: 2rem border #444444;
  margin-right: 1rem;
  padding: 1rem .5rem 1rem;
  style: inline-block;
}
</style>
