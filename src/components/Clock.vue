<template>
  <div>
    <div class="container">
      <p class="location">{{ location }}</p> 
      <p class="date">{{ year }}/{{ month }}/{{ day }}</p>
      <div class="time">
        <p class="time-item hours">{{ hours }}</p>
        <p class="time-item minutes">{{ minutes }}</p>
        <p class="time-item seconds">{{ seconds }}</p>
      </div>
    </div>
  </div>
</template>

<script>
const zeroPadding = (num, digit) => {
  return (Array(digit).join("0") + num).slice(-digit)
}

export default {
  props: ["location", "diff"],
  data() {
    return {
      date: new Date(),
    }
  },
  computed: {
    year() {
      return this.date.getFullYear()
    },
    month() {
      return zeroPadding(this.date.getMonth() + 1, 2)
    },
    day() {
      return zeroPadding(this.date.getDate(), 2)
    },
    hours() {
      return zeroPadding(this.date.getHours(), 2)
    },
    minutes() {
      return zeroPadding(this.date.getMinutes(), 2)
    },
    seconds() {
      return zeroPadding(this.date.getSeconds(), 2)
    },
  },
  mounted() {
    this.setDate()
    setInterval(() => this.setDate(), 1000)
  },
  methods: {
    setDate() {
      this.date = new Date()
      this.date.setHours(this.date.getHours() + this.diff)
    },
  },
}
</script>

<style scoped>
</style>
