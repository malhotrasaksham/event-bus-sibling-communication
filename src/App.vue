<template>
  <div id="app">
    <h2>Parent</h2>
    <p>Age is {{age}}</p>
    <hr>
    <first></first>
    <hr>
    <second></second>
  </div>
</template>

<script>
import First from "@/components/child1";
import Second from "@/components/child2";

export default {
  name: "App",
  components: {
    First,
    Second
  },
  data() {
    return {
      age: 4
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
