<template>
  <div class="hello">
    <p>My name is {{ name }}</p>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  setup() {
    console.log("setup function!!");
    let name = "Paul";
    // let age = 21;

    return { name: name };
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
