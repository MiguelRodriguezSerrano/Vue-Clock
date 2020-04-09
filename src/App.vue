<template>
  <div id="app" :class="mode">
    <Header></Header>
    <Clock></Clock>
  </div>
</template>

<script>
import Clock from "./components/Clock.vue";
import Header from "./components/Header";
export default {
  name: "App",
  components: {
    Header,
    Clock
  },
  data() {
    return {
      mode: "dark"
    };
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
#app {
  overflow: hidden;
  background: #bfa788;
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.dark {
  overflow: hidden;
  background: #333;
  width: 100%;
  height: 100vh;
  display: flex;
  color: red;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
