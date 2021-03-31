<template>
  <!-- Latest compiled and minified CSS -->
  <link
    rel="stylesheet"
    href="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css"
  />
  <nav-bar @change-page="activePage"></nav-bar>
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
  <div id="landingPage" v-if="homeIsActive">
    <LandingPage msg="Hi I'm Esben" />
  </div>

  <div id="resume" v-if="resumeIsActive">
    <resume></resume>
  </div>

  <div id="blog" v-if="blogIsActive">
    <blog></blog>
  </div>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import LandingPage from "./components/LandingPage.vue";
import Blog from "./components/Blog.vue";
import Resume from "./components/Resume.vue";
export default {
  name: "App",
  components: {
    LandingPage,
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

.footer {
  position: absolute;
  bottom: 10px;
  width: 50%;
}
</style>
