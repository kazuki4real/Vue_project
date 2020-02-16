<template>
<div>
  <div class="container">
    <p class="date">{{date}}</p>
    <div class="time">
      <p class="time-item hours">{{hour}}</p>
      <p class="time-item minutes">{{minute}}</p>
      <p class="time-item seconds">{{second}}</p>
    </div>
  </div>
</div>
</template>

<style scoped>
  .container {
  background-color: #3a4a5e;
  padding: 2%;
}
 
 
.date {
  text-align: right;
  color: #fff;
  font-family: 'Teko', sans-serif;
  font-size: 4rem;
  letter-spacing: .1em;
  margin: .0em 0;
  line-height: 1;
}
 
 
.time {
  display: flex;
}


.time-item {
  display: flex;
  justify-content: center;
  align-items: center;
  flex: 1 1;
  height: 100px;
  position: relative;
  z-index: 1;
  padding: 0.5em;
  margin: 3px;
  color: #fff;
  font-family: 'Roboto Mono', monospace;
  font-size: 3rem;
  line-height: 1;
  background-color: #48b883;
  box-sizing: border-box;
}
 
 
.time-item:before {
  position: absolute;
  right: 5px;
  bottom: 1px;
  z-index: 1;
  color: #3a4a5e;
  font-family: 'Teko', sans-serif;
  font-size: 1.4rem;
  letter-spacing: .05em;
}
 
 
.hours:before {
  content: "Hours";
}
 
 
.minutes:before {
  content: "Minutes";
}
 
 
.seconds:before {
  content: "Seconds";
}
</style>
<script>
  // const zeroPadding = (num, digit) =>
  //   (Array(digit).join('0') + num).slice(-digit);


  export default {
    data() {
      return {
        date: new Date(),
      }
    },
    computed: {
      year: function() {
        return this.date.getFullYear()
      },
      month: function() {
        return this.date.getMonth() + 1
      },
      day: function() {
        return this.date.getDate()
      },
      hour: function() {
        return this.date.getHours()
      },
      minute: function() {
        return this.date.getMinutes()
      },
      second: function() {
        return this.date.getSeconds()
      },
      },
      methods: {
        setDate() {
          this.date = new Date()
        }
      }
  }
</script>