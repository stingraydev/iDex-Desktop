<template>
  <div id="app">
    <desktop></desktop>
  </div>
</template>

<script>
import desktop from "./components/desktop";

export default {
  name: "app",
  components: {
    desktop
  }
};
</script>

<style>
  body, h1, h2 {
    margin: 0;
    padding: 0;
  }
  body {
    font-family: 'Open Sans', sans-serif;
    font-style: normal;
    font-weight: 400;
    background-color: #F7F7F7;
}
</style>
