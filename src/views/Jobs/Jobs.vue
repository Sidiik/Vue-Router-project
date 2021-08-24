<template>
  <h1>Jobs</h1>
  <div v-for="job in jobs" :key="job.id">
    <h1>{{ job.title }}</h1>
  </div>
</template>

<script>
import JobDetails from "./JobDetails.vue";
export default {
  name: "Jobs",
  components: { JobDetails },
  data() {
    return {
      jobs: [
        {
          id: 1,
          title: "Vue web developer",
        },
        {
          id: 2,
          title: "UI react developer",
        },
      ],
    };
  },
};
</script>

<style></style>
