<template>
  <button
    type="submit"
    class="SubmitButton"
    v-on:click="onClick"
  >{{ text }}
  </button>
</template>

<script>
import Vue from "vue";

export default {
  props: {
    text: {
      type: String,
      default: "Search",
    },
  },
  methods: {
    onClick() {
      this.$emit("click");
    },
  },
};
</script>

<style scoped>
.SubmitButton {
  min-width: 8rem;
  border-radius: 30rem;
  background-color: #FFD700;
  border: none;
  color: #444444;
  padding: 1rem 2rem;
  font-weight: bold;
  font-size: 1.5rem;
  display: inline-block;
  cursor: pointer;
}
.SubmitButton:hover {
  background-color: #DDDDDD;
}
</style>
