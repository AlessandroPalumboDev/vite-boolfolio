<script>
// import HelloWorld from "./components/HelloWorld.vue";
import axios from "axios";
export default {
  name: "Projects",
  data() {
    return {
      title: "Projects",
      projects: [],
    };
  },
  methods: {
    getProjects() {
      axios
        .get("http://127.0.0.1:8000/api/projects")
        .then((response) => {
          this.projects = response.data.results;
          console.log(this.projects);
        })
        .catch((error) => console.log(error));
    },
  },
  created() {
    this.getProjects();
  },
};
</script>

<template>
  <header>
    <div class="container">
      <div class="row">
        <div class="col text-center">
          <h1>header</h1>
        </div>
      </div>
    </div>
  </header>

  <main>
    <div class="container">
      <div class="row">
        <div class="col text-center">
          <h2>{{ title }}</h2>
        </div>
      </div>
    </div>
  </main>

  <footer>
    <div class="container">
      <div class="row">
        <div class="col text-center text-secondary">
          <h2>footer</h2>
          <span class="text-body-tertiary py-3 m-2">
            <font-awesome-icon :icon="['fas', 'fa-user-secret']" />
            AP
          </span>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
h1 {
  color: red;
}
main {
  h2 {
    color: blue;
  }
}
</style>
