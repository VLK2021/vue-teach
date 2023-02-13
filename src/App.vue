<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <div>Hello world from {{ name }}</div>

  <div>
    <img :src="img" v-bind:alt="`alt is: ${alt}`" />
  </div>

  <!--first variant-->
  <!--  <button @click="name = Math.floor(Math.random() * 1000)">change name</button>-->

  <!--  second variant-->
  <button @click="changeName">change name</button>

  <!--  <ButtonTest :text="`my awesome button!`" :onClick="changeName" />-->
  <ButtonTest :text="`my awesome button!`" @button-click="changeName" />
</template>

<script>
import ButtonTest from "@/components/ButtonTest";

export default {
  name: "App",
  components: {
    ButtonTest,
  },
  data() {
    return {
      name: "Volodymyr",
      img:
        "https://img.freepik.com/premium-photo/phoenix-bird-fire-mythological-fenix-bird-with-\n" +
        "    flames-fantasy-illustration_691560-3551.jpg",
      alt: "Fenix",
    };
  },

  methods: {
    changeName() {
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
img {
  width: 11rem;
}
</style>
