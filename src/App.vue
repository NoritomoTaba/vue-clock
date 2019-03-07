<template>
<div>
  <!--<input v-model="location"></input>-->
  <!--<SearchForm
    v-model="location"
    v-on:input="onInput"
    v-on:click="onClick"
  />-->
  <input v-model="value" placeholder="please input here"/>
  <SubmitButton v-on:click="onClick" />
  <Clock :location="location" diff="0"></Clock>
</div>
</template>

<script>
import Vue from "vue";
import TextField from "./components/TextField.vue";
import SearchForm from "./components/SearchForm.vue";
import Clock from "./components/Clock.vue";
import Print from "./components/Print.vue";
import SubmitButton from "./components/SubmitButton.vue";

export default Vue.extend({
  props: {
    value: {
      type: String,
    },
    location: {
      type: String,
      default: "TOKYO",
    },
  },
  components: {
    Clock,
    TextField,
    SearchForm,
    Print,
    SubmitButton,
  },
  methods: {
    onClick() {
      this.location = this.value
    },
  },
});
</script>

<style scoped>
.clock {
  width: 80%;
  max-width: 300rem;
  margin: 30px auto;
}
</style>

<style>
html {
  font-size: 62.5%;
  background-color: #444444;
}
 
body {
  margin: 0;
}

</style>
