<template>
  <header>
    <link
      rel="stylesheet"
      href="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.10.1/devicon.min.css"
    />
  </header>
  <div class="hello" :style="{ color: textColor }">
    <h1>Blog</h1>
    <p>The projects I am or have been working on will be posted here</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      textColor: "grey",
    };
  },
};
</script>