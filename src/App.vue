<template>
  <header>
    <head>
      <title>Esben's blog</title>
      <!-- Latest compiled and minified CSS -->
    </head>
    <link
      rel="stylesheet"
      href="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css"
    />
  </header>
  <body>
    <nav-bar @change-page="activePage"></nav-bar>
    <br /><br />

    <div id="landingPage" v-if="homeIsActive">
      <home></home>
    </div>

    <div id="resume" v-if="resumeIsActive">
      <resume></resume>
    </div>

    <div id="blog" v-if="blogIsActive">
      <blog></blog>
    </div>
    <br />
    <br />
  </body>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import Home from "./components/Home.vue";
import Blog from "./components/Blog.vue";
import Resume from "./components/Resume.vue";
export default {
  name: "App",
  components: {
    Home,
    NavBar,
    Resume,
    Blog,
  },
  data() {
    return {
      page: "home",
      homeIsActive: true,
      resumeIsActive: false,
      blogIsActive: false,
    };
  },
  methods: {
    // Gets the checkbox information from the child component
    activePage(params) {
      this.page = params;
    },
  },
  watch: {
    page: function () {
      if (this.page === "home") {
        this.homeIsActive = true;
        this.resumeIsActive = false;
        this.blogIsActive = false;
      } else if (this.page === "resume") {
        this.homeIsActive = false;
        this.resumeIsActive = true;
        this.blogIsActive = false;
      } else if (this.page === "blog") {
        this.homeIsActive = false;
        this.resumeIsActive = false;
        this.blogIsActive = true;
      }
    },
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
  margin-top: 0px;
}
</style>

<style scoped>
body {
  margin: 0px;
  height: 140vh;
  background-color: lightgrey;
}
</style>