<template>
  <div id="app">
    <img width="25%" src="./assets/logo.png">
    <!-- <HelloWorld msg="Hello Vue + Composition API in CodeSandbox!"/> -->
    <Tester/>
    <Counter title="Hello World"/>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import Counter from "./components/CompositionCounter";
import Tester from "./components/Tester";

export default {
  name: "App",
  components: {
    HelloWorld,
    Counter,
    Tester
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
