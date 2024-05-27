<template>
  <div id="app">
    <ParentComponent @show-data="showDataFromChild" />
    <p>Data from all child components: {{ dataFromChild }}</p>
  </div>
</template>

<script>
import ParentComponent from "./components/ParentComponent.vue";

export default {
  name: "App",
  components: {
    ParentComponent,
  },
  data() {
    return {
      dataFromChild: "",
    };
  },
  methods: {
    showDataFromChild(data) {
      this.dataFromChild += data + " ";
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
