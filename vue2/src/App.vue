<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <div>
      <button v-on:click="plus">Plus</button>
      <button v-on:click="something">Change name</button>
      <p>{{ title }}</p>
      <p>{{ test.number }}</p>
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

let test = { number: 1 }

export default {
  name: "App",
  components: {
    HelloWorld,
  },
  data: () => {
    return {
      title: "Hello World",
      test
    }
  },

  props: {

  },
  methods: {
    plus() {
      test.number++;
    },
    something() {
      this.title = this.title + " Yhonatan";
    }
  },
  watch: {
    a: function(val, oldVal) {
      console.log('new: %s, old: %s', val, oldVal);
    }
  }
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
