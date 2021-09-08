<template>
  <div id="app">
    <button @click="getData">Get data</button>
  </div>
</template>

<script>
/* eslint-disable */
export default {
  name: "app",
  methods: {
    async getData() {
      const data = await fetch("/api/info").then((res) => res.json());
      console.log(data);
    },
  },
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
