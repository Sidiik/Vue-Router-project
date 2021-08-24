<template>
  <h1>Jobs</h1>
  <div v-for="job in jobs" :key="job.id" class="job">
    <router-link :to="{ name: 'JobDetails', params: { id: job.id } }">
      <h1>{{ job.title }}</h1>
    </router-link>
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
        {
          id: 3,
          title: "UX react developer",
        },
      ],
    };
  },
};
</script>

<style>
.job {
  background: #eee;
  width: 30%;
  margin: auto;
  padding: 1px;
  margin-top: 10px;
  border-radius: 0.3rem;
  cursor: pointer;
}
.job:hover {
  background: #444;
  color: #fff;
}
.job a {
  text-decoration: none;
  color: gray;
}
</style>
