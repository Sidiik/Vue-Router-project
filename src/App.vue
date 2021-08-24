<template>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link :to="{ name: 'About' }">About</router-link>
    <router-link :to="{ name: 'Jobs' }">Jobs</router-link>
  </div>
  <button @click="redirect">Redirect</button>
  <button @click="back">Go back</button>
  <button @click="forward">Forward</button>
  <router-view />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
  padding: 10px;
  text-decoration: none;
  transition: all 0.3s ease-in;
  border-radius: 0.5rem;
}

#nav a.router-link-exact-active {
  color: #42b983;
  background: crimson;
  color: white;
}
button {
  background: rgb(10, 190, 100);
  border: 0;
  outline: 0;
  margin-left: 1rem;
  padding: 0.4rem 0.6rem;
  font-weight: 800;
  border-radius: 30px;
  cursor: pointer;
  color: #fff;
  transition: 0.4s ease;
}
button:hover {
  background: rgb(19, 238, 129);
}
</style>

<script>
export default {
  methods: {
    redirect() {
      this.$router.push({ name: "Home" });
    },
    back() {
      this.$router.go(-1);
    },
    forward() {
      this.$router.go(1);
    },
  },
};
</script>
