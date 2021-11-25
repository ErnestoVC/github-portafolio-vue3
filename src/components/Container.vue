<template>
  <div id="container" class="container">
    <img
      src="https://avatars.githubusercontent.com/u/26695194?v=4"
      alt="Avatar de ErnestoVC"
      width="250"
      loading="lazy"
      class="image"
    />
    <h2>Proyectos</h2>
    <hr />
    <loading v-if="load" />
    <br />
    <div class="cards" v-for="project in projects" :key="project.id">
      <Card
        :name="project.name"
        :description="project.description"
        :author="project.owner.login"
        :url="project.html_url"
        :homepage="project.homepage"
      />
    </div>
  </div>
</template>

<script>
import Card from "./Card.vue";
import Loading from "./Loading.vue";
export default {
  data() {
    return {
      projects: null,
      load: false,
    };
  },
  components: {
    Card,
    Loading,
  },
  mounted() {
    this.getProjects();
  },
  methods: {
    async getProjects() {
      this.load = true;
      const res = await fetch("https://api.github.com/users/ErnestoVC/repos");
      const data = await res.json();
      this.projects = data;
      this.load = false;
    },
  },
};
</script>

<style scoped>
.image {
  border-radius: 50%;
}
.cards {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
.container {
  border: solid 1px #eee;
  box-shadow: 1px 1px 1px 4px #333;
  text-align: center;
  overflow: hidden;
}
</style>
