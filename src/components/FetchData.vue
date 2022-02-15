<template>
  <div>
    <div v-if="show">
      <Props />
    </div>
    <button @click="Click">Unmount Component</button>
  </div>
</template>

<script>
import { onMounted, onUnmounted, ref } from "@vue/runtime-core";
import Props from "./Props.vue";
export default {
  name: "FetchData",
  components: { Props },
  setup() {
    onMounted(() => console.log("component mounted"));
    onUnmounted(() => console.log("component unmounted"));
    // run when any data in this component updated
    // onUpdated(() => console.log("component updated"));
    const show = ref(true);
    const Click = () => {
      show.value = !show.value;
    };
    return { Click, show };
  },
};
</script>

<style></style>
