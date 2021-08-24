<template>
  <h1>Job details</h1>
  <p>
    {{ title }}
  </p>
</template>

<script>
export default {
  name: "Details",
  props: ["title"],
};
</script>

<style scoped>
p {
  border: 1px solid crimson;
  width: 30%;
  margin: auto;
  padding: 1rem;
  border-radius: 0.5rem;
}
</style>
