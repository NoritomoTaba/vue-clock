<template>
  <div class="SearchForm">
    <TextField
    placeholder="都市名を入力してください"
    v-model="text"></TextField>
    <SubmitButton v-on:click="onClick"></SubmitButton>
  </div>
</template>

<script>
import Vue from "vue";
import TextField from "./TextField.vue";
import SubmitButton from "./SubmitButton.vue";

export default Vue.extend({
  name: "SearchForm",
  components: {
    SubmitButton,
    TextField,
  },
  props: {
    text: {
      type: String,
    },
  },
  methods: {
    onClick() {
      this.$emit("click", this.text);
    },
  },
});
</script>

<style>
.SearchForm {
  display: flex;
  justify-content: center;
}

</style>
