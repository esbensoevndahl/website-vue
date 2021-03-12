<template>
  <!-- Latest compiled and minified CSS -->
  <link
    rel="stylesheet"
    href="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css"
  />
  <svg
    xmlns="http://www.w3.org/2000/svg"
    width="32"
    height="32"
    fill="currentColor"
    class="bi bi-laptop"
    viewBox="0 0 16 16"
  >
    <path
      d="M13.5 3a.5.5 0 0 1 .5.5V11H2V3.5a.5.5 0 0 1 .5-.5h11zm-11-1A1.5 1.5 0 0 0 1 3.5V12h14V3.5A1.5 1.5 0 0 0 13.5 2h-11zM0 12.5h16a1.5 1.5 0 0 1-1.5 1.5h-13A1.5 1.5 0 0 1 0 12.5z"
    />
  </svg>
  
  <Welcome msg="Hi I'm Esben" />
</template>

<script>
import Welcome from "./components/Welcome.vue";
export default {
  name: "App",
  components: {
    Welcome,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Verdana, Tahoma, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
