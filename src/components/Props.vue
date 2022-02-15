<template>
  <div><h1>Props Component</h1></div>
</template>

<script>
import { onMounted, onUnmounted } from "@vue/runtime-core";
export default {
  name: "Props",
  setup() {
    onUnmounted(() => console.log("props component unmounted"));
    onMounted(() => console.log("props component mounted"));
  },
};
</script>

<style></style>
