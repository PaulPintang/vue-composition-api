<template>
  <div>
    <button @click="click"></button>
    <Props name="Paul" />
  </div>
</template>

<script>
// import { methods } from "vue";
import Props from "./Props.vue";
export default {
  name: "FetchData",
  components: { Props },
  setup() {
    const click = () => {
      alert("sdsad");
    };
    return { click };
  },
};
</script>

<style></style>
