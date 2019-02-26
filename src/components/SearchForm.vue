<template>
  <div class="SearchForm">
    <TextField
    placeholder="都市名を入力してください"></TextField>
    <SubmitButton></SubmitButton>
  </div>
</template>

<script>
import Vue from "vue";
import TextField from "./TextField.vue";
import SubmitButton from "./SubmitButton.vue";

export default {
  components: {
    SubmitButton,
    TextField,
  },
  methods: {
    onClick() {
      this.$emit("click");
    },
  },
};
</script>

<style>
.SearchForm {
  display: flex;
  justify-content: center;
}

</style>
