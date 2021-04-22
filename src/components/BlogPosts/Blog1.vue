<template>
  <header>
    <link
      rel="stylesheet"
      href="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.10.1/devicon.min.css"
    />
  </header>
  <body>
    <div class="hello" :style="{ color: textColor }">
    </div>
  </body>
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

<style scoped>
body {
  overflow-x: hidden;
  margin-left: 100px;
  margin-right: 100px;
  background-color: white;
}
</style>