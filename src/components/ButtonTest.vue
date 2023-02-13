<template>
  <!--  <button @click="onClick">{{ text }}</button>-->
  <button class="btn" @click="onClickHandler">{{ text }}</button>
</template>

<script>
export default {
  name: "ButtonTest",
  emits: ["button-click"],
  props: {
    text: {
      type: String,
      required: true,
    },
    // onClick: {
    //   type: Function,
    //   required: true,
    // },
  },
  methods: {
    onClickHandler() {
      this.$emit("button-click");
    },
  },
};
</script>

<style scoped>
.btn {
  padding: 6px 10px;
  display: flex;
  background: snow;
  align-items: center;
  justify-content: center;
  border: 1px solid black;
  text-transform: uppercase;
  font-weight: bold;
  transition: 0.2s;
}

.btn:hover {
  transform: scale(1.01, 1.01);
}
</style>
