<template>
  <div id="app">
    <h1>{{ number }}</h1>
     <button v-on:click="plus1">Add 1</button>
      <button v-on:click="minus1">Subtract 1</button>
  </div>
</template>

<script>
import { increment, decrement } from "./library/logic.ml";

export default {
  name: "app",
  data() {
    return {
      number: 0
    };
  },
  methods: {
    plus1: function(e) {
      this.number = increment(this.number);
    },
    minus1: function(e) {
      this.number = decrement(this.number);
    }
  }
};
</script>

<style lang="css">
#app {
  font-size: 30px;
  color: var(--main-color);
}
</style>


