<template>
  <div class="hello" :style="{ color: textColor }">
    <h1>{{ msg }}</h1>
    <p>
      - and this is my personal website. <br />
      I study Computer Science and work on various project in my free time.
      <br />
      I recently started learning Vue.js, which is what this website has been
      built with.
    </p>

    <div class="absolute">
      <h1>Content</h1>
      <div class="row">
        <div class="col-xs-4"><h3>Home</h3></div>
        <div class="col-xs-4"><h3>Resume</h3></div>
        <div class="col-xs-4"><h3>Blog</h3></div>
      </div>
    </div>
  </div>

  <button type="button" class="btn btn-light">
    Toggle dark mode
  </button>
  <br><br>
  <button type="button" class="btn btn-light" @click="showColors()">
    Change font color
  </button>
  <ul v-show="showColor">
    <li
      v-for="textColor in colors"
      :key="textColor"
      :style="{ backgroundColor: textColor }"
      @mouseover="changeColor(textColor)"
      class="color-box"
      float:left
    ></li>
  </ul>
</template>

<script>
export default {
  name: "Welcome",
  props: {
    msg: String,
  },
  data() {
    return {
      showColor: false,
      textColor: "Grey",
      colors: [
        "Aquamarine",
        "Black",
        "Brown",
        "Coral",
        "Gold",
        "Grey",
        "Orange",
        "Tomato",
      ],
    };
  },
  methods: {
    changeColor(input) {
      this.textColor = input;
    },
    showColors() {
      this.showColor = !this.showColor;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
div.absolute {
  position: center;
  margin-top: 100px;
  margin-bottom: 50px;
}
.color-box {
  width: 40px;
  height: 40px;
  margin-top: 5px;
}
ul {
  justify-content: center;
  display: flex;
}
li {
  position: center;
  float: left;
  list-style-type: none;
}
</style>
