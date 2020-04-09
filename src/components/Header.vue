<template>
  <div>
    <h1>{{title}}</h1>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      title: "Vue Awesome Clock!"
    };
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap");
h1 {
  position: relative;
  bottom: 100%;
  font-family: "Montserrat", sans-serif;
  font-size: 2em;
  color: #fff;
}
</style>