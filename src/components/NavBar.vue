<template>
  <link
    rel="stylesheet"
    href="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css"
  />
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav mr-auto">
        <li class="nav-item active">
          <a class="nav-link" href="#" @click="showHome()">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#" @click="showResume()">Resume</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#" @click="showBlog()">Blog</a>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: "navBar",
  data() {
    return {
      active: "home",
    };
  },
  methods: {
    showResume() {
      this.active = "resume";
      this.$emit("change-page", "resume");
    },
    showHome() {
      this.active = "home";
      this.$emit("change-page", "home");
    },
    showBlog() {
      this.active = "blog";
      this.$emit("change-page", "blog");
    },
  },
};
</script>
