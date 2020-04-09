<template>
  <div class="clock">
    <div class="hours">{{ hours }}</div>
    <div class="sep">:</div>
    <div class="minutes">{{ minutes }}</div>
    <div class="sep">:</div>
    <div class="seconds">{{ seconds }}</div>
    <div class="mode">{{ mode }}</div>
  </div>
</template>

<script>
export default {
  name: "Clock",
  props: {
    msg: String
  },
  data() {
    return {
      hours: "--",
      minutes: "--",
      seconds: "--"
    };
  },
  mounted() {
    setInterval(() => this.updateDate(), 1000);
  },
  methods: {
    updateDate() {
      const date = new Date();
      this.hours = this.toHuman(date.getHours());
      this.minutes = this.toHuman(date.getMinutes());
      this.seconds = this.toHuman(date.getSeconds());
    },
    toHuman(v) {
      return v.toString().padStart(2, "0");
    },
    test() {
      alert("EY!");
    }
  },
  computed: {
    mode() {
      return this.hours <= 12 ? "AM" : "PM";
    }
  }
};
</script>


<style>
.clock {
  font-family: "Montserrat", sans-serif;
  font-size: 2em;
  width: 30%;
  height: 20vh;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #fff;
  border-radius: 35px;
  background: linear-gradient(225deg, #ccb392, #ac967a);
  box-shadow: -28px 28px 56px #a89378, 28px -28px 56px #d6bb98;
}
</style>

