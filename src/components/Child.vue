<template>
  <li>
    <div>Child Comp</div>
    <div>User Name: {{name}}</div>
    <div>Reverse Name: {{switchName()}}</div>
  </li>
</template>

<script>
export default {
  name: "Child",
  props: {
    name: {
      type: String,
      required: true
    }
  },
  methods: {
    switchName() {
      const { name } = this;
      return name
        .split("")
        .reverse()
        .join("");
    }
  }
};
</script>

<style scoped>
p {
  color: #d7dadc;
  margin-bottom: 1rem;
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