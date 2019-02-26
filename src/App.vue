<template>
  <div>
    <!--<TextField></TextField>
    <SubmitButton></SubmitButton>-->
    <Clock location="TOKYO" :diff="0"/>
  </div>
</template>

<!--
    <Clock location="TOKYO" :diff="0"/>
    <Clock class="clock" location="NY" :diff="-14"/>
    <Clock class="clock" location="LA" :diff="-17"/>
    <Clock class="clock" location="UK" :diff="-9"/>
    <Clock class="clock" location="BRAZIL" :diff="-12"/>
    <Clock class="clock" location="SYDNEY" :diff="1"/>
    <Clock class="clock" location="DUBAI" :diff="-5"/>
    <Clock class="clock" location="JOHANNESBURG" :diff="-7"/>
-->

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
}
 
body {
  margin: 0;
}

</style>
