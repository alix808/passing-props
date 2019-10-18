<template>
  <div>
    <h1>Using Props for Parent => Child Communication</h1>
    <ul>
      <li>
        <h1>Parent Comp</h1>
        <button @click="changeName">Change my name</button>
      </li>
      <Child :name="name" />
    </ul>
  </div>
</template>

<script>
import Child from "./Child";

export default {
  name: "Parent",
  components: { Child },
  data: () => ({
    name: "Max"
  }),
  methods: {
    changeName() {
      this.name = "Anna";
    }
  }
};
</script>

<style scoped>
h1 {
  font-size: 16px;
  padding: 1rem 0rem;
  color: #d7dadc;
}
ul {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 1rem;
}
li {
  border: 1px solid #343536;
  border-radius: 2px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #d7dadc;
  background: #1a1a1b;
  padding: 1rem;
}
li:hover {
  border: 1px solid white;
}
button {
  background: #d7dadc;
  text-transform: uppercase;
  padding: 1rem 0.5rem;
  border-radius: 4px;
}
button:focus {
  outline: 0;
}
</style>