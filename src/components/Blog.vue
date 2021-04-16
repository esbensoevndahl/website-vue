<template>
  <header>
    <link
      rel="stylesheet"
      href="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.10.1/devicon.min.css"
    />
  </header>
  <body>
    <div class="hello" :style="{ color: textColor }">
      <h1>Blog</h1>
    <blog-1></blog-1>
    </div>
  </body>
</template>

<script>
import Blog1 from "./BlogPosts/Blog1.vue";
export default {
  components: { Blog1 },
  data() {
    return {
      textColor: "grey",
    };
  },
};
</script>

<style scoped>
body {
  overflow-x: hidden;
  margin-left: 100px;
  margin-right: 100px;
  background: white;
}
</style>