<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <div>Hello world from {{ name }}</div>

  <button @click="changeName(123, $event)">change name</button>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "Volodymyr",
    };
  },

  methods: {
    changeName(arg, event) {
      console.log(arg, event);
      this.name = Math.floor(Math.random() * 1000);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
