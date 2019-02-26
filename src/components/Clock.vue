<template>
  <div>
    <div class="container">
      <div class="detail">
        <p class="location">{{ location }}</p> 
        <p class="date">{{ year }}/{{ month }}/{{ day }}</p>
      </div>
      <div class="time">
        <p class="time-item hours">{{ hours }}:</p>
        <p class="time-item minutes">{{ minutes }}:</p>
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
.container {
  font-family:'Lato', 'Noto Sans JP', '游ゴシック Medium', '游ゴシック体', 'Yu Gothic Medium', YuGothic, 'ヒラギノ角ゴ ProN', 'Hiragino Kaku Gothic ProN', 'メイリオ', Meiryo, 'ＭＳ Ｐゴシック', 'MS PGothic', sans-serif;
}

.location {
  color: #DDDDDD;
  font-size: 6rem;
  padding: 1rem;
  margin-left: auto;
  margin-top: .5rem;
  margin-bottom: 0rem;
  text-align: center;
}

.date {
  color: #DDDDDD;
  font-size: 3rem;
  padding-bottom: 0rem;
  margin-right: auto;
  margin-top: 0rem;
  margin-bottom: .5rem;
  text-align: center;
}

.time {
  display: flex;
}
.time-item {
  font-size: 10rem;
  margin-top: 0rem;
  margin-bottom: .5rem;
  color: #DDDDDD;
}
.hours {
  margin-left: auto;
  margin-right: 1rem;
}
.minutes {
  margin-right: 1rem;
}
.seconds {
  margin-right: auto;
}
</style>

