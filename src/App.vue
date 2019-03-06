<template>
<div>
  <input v-model="location"></input>
  <Clock :location="location" diff="0"></Clock>
</div>
</template>

<script>
import Vue from "vue";
//import SearchForm from "./components/SearchForm.vue";
import Print from "./components/Print.vue";
import Clock from "./components/Clock.vue";

export default Vue.extend({
  props: {
    location: {
      type: String,
      default: "TOKYO",
    },
  },
  components: {
    Print,
    Clock,
 //   SearchForm,
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
