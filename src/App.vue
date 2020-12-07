<template>
  <div id="app">
    <TestComponent/>
    <Counter></Counter>
    <HelloComponent></HelloComponent>
    <HelloWorld msg="Welcome to Your Vue.js App"/>

  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TestComponent from "@/components/TestComponent";
import Counter from "@/components/Counter";
import HelloComponent from "@/components/HelloComponent";

export default {
  name: 'App',
  components: {
    HelloComponent,
  }
}
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
