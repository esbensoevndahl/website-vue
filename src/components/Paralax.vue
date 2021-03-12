<template>
  <div class="sidebar">
    <ul class="sidebar__nav">
      <li :class="{ selected: selected === 0 }" @click="changeSelected(0)">
        <i class="fas fa-th"></i>
        Dashboard
      </li>
      <li :class="{ selected: selected === 1 }" @click="changeSelected(1)">
        <i class="fas fa-paperclip"></i>
        Links
      </li>
      <li><i class="fas fa-sitemap"></i>Visualization</li>
      <li><i class="fas fa-sliders-h"></i>Settings</li>
      <ul>
        <!-- after all the <li> -->
        <div class="select-highlight" />
      </ul>
    </ul>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  setup() {
    const selected = ref(0); // index of the selected el

    const changeSelected = (i) => {
      selected.value = i;
      document.getElementsByClassName('select-highlight')[0].style.top = i * 50 + 5 + 'px'
    };
    return {
      changeSelected,
      selected,
    };
  },
};
</script>

<style lang="scss" scoped>
.sidebar {
  height: 100vh;
  max-height: 100vh;
  overflow: hidden;
  position: relative;
  width: 300px;
  font-size: 1.2em;
  background-color: #fff;
  padding: 30px 0 0 30px;
  box-sizing: border-box;
  float: left;
}
.select-highlight {
      position: absolute;
      right: 0;
      top: 5px;
      height: 30px;
      width: 4px;
      background-color: #4bcffa;
      transition: 0.1s top ease-out;
}

ul.sidebar__nav {
  width: 100%;
  position: relative;

  li {
    margin-bottom: 10px;
    padding: 10px 0;
    font-size: 0.9em;
    color: #d2dae2;
    cursor: pointer;

    &.selected {
      color: #4bcffa;
    }

    i {
      width: 40px;
      color: inherit;
    }
  }
}
</style>