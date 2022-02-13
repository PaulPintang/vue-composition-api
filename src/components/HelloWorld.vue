<template>
  <div class="hello">
    <h1>Array</h1>
    <input type="text" v-model="search" />
    <p>search term - {{ search }}</p>
    <div v-for="name in searchName" :key="name">
      <p>{{ name }}</p>
    </div>
    <!-- <h1>Filtered Array</h1>
    <div v-for="name in filteredNames" :key="name">
      <p>{{ name }}</p>
    </div> -->
  </div>
</template>

<script>
import { ref, computed } from "@vue/reactivity";
export default {
  name: "HelloWorld",
  setup() {
    const names = ref(["paul", "john", "doe", "peter"]);

    const search = ref("");
    const searchName = computed(() => {
      return names.value.filter((name) => name.includes(search.value));
    });
    return { names, search, searchName };
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
