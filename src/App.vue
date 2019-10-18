<template>
  <div class="container">
    <div class="flex">
      <Parent />
    </div>
  </div>
</template>

<script>
import Parent from "./components/Parent.vue";

export default {
  name: "app",
  components: { Parent }
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.4;
  background: #030303;
}
.container {
  max-width: 1100px;
  margin-left: auto;
  margin-right: auto;
}

.flex {
  opacity: 0.4;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  height: 800px;
}
</style>
