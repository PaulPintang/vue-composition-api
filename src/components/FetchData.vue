<template>
  <div>
    <Props name="Paul" />
  </div>
</template>

<script>
import { onMounted, onUnmounted, onUpdated } from "@vue/runtime-core";
// import { methods } from "vue";
import Props from "./Props.vue";
export default {
  name: "FetchData",
  components: { Props },
  setup() {
    onMounted(() => console.log("component mounted"));
    onUnmounted(() => console.log("component unmounted"));
    onUpdated(() => console.log("component updated"));
  },
};
</script>

<style></style>
