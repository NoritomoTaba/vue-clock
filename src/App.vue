<template>
  <div>
    <Clock location="TOKYO" :diff="0"/>
  </div>
</template>

<script>
import Vue from "vue";
import Clock from "./components/Clock.vue"
import TextField from "./components/TextField.vue";
import SubmitButton from "./components/SubmitButton.vue";

export default {
  components: {
    Clock,
    TextField,
    SubmitButton,
  },
}
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
