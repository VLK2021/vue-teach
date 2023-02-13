<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <button @click="increment">increment</button>

  <div>{{ counter }}</div>

  <button @click="decrement">decrement</button>
  <button @click="reset">reset</button>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      counter: 0,
    };
  },

  methods: {
    increment() {
      this.counter += 1;
    },
    decrement() {
      this.counter -= 1;
    },
    reset() {
      this.counter = 0;
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
img {
  width: 10rem;
}
</style>
