<template>
  <div v-if="job">
    <h1>Job Details</h1>
    <h1>{{ job.title }}</h1>
    <h3>{{ job["Job type"] }}</h3>
    <p>the id is {{ job.id }}</p>
  </div>
  <div v-else>
    <p>Loading...</p>
  </div>
</template>

<script>
export default {
  props: ["id"],
  mounted() {
    fetch("http://localhost:3000/Jobs/" + this.id)
      .then((res) => res.json())
      .then((data) => (this.job = data));
  },
  data() {
    return {
      job: null,
    };
  },
};
</script>

<style></style>
