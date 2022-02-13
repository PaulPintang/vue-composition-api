<template>
  <div class="hello">
    <p ref="p">My name is {{ name }}</p>
    <button @click="click">Click me</button>
  </div>
</template>

<script>
import { ref } from "@vue/reactivity";
export default {
  name: "HelloWorld",
  setup() {
    let name = ref("Paul");
    const p = ref(null);
    const click = () => {
      name.value = "dsdasdssss";
    };
    return { name, p, click };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
