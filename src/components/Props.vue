<template>
  <div>props component</div>
</template>

<script>
export default {
  name: "Props",
  props: { name },
  setup(props) {
    console.log(props.name);
  },
};
</script>

<style></style>
