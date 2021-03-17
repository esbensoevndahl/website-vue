<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      - and this is my personal website. <br />
      I study Computer Science and work on various project in my free time.
    </p>

    <div id="content" class="container">
      <h1>Content</h1>
      <div class="row">
        <div class="col-xs-4"><h3>Home</h3></div>
        <div class="col-xs-4"><h3>Resume</h3></div>
        <div class="col-xs-4"><h3>Blog</h3></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Welcome",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
</style>
