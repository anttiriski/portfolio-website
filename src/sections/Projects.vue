<template>
  <div class="projects-container">
    <div>
      <h3 class="project-header">My Projects</h3>
    </div>
    <div class="project-grid">
      <ProjectModal
        v-for="(project, index) in projectData"
        :key="index"
        :project="project"
      />
    </div>
  </div>
</template>

<script>
import ProjectModal from "../components/ProjectModal";
import data from "../data.json";
export default {
  name: "Projects",
  data() {
    return {
      projectData: data.projects,
    };
  },
  components: {
    ProjectModal,
  },
};
</script>

<style>
.project-header {
  color: #222222;
  font-weight: 700;
  font-size: 45px;
  line-height: 44px;
  position: relative;
}
.project-header::after {
  position: absolute;
  content: "";
  height: 3px;
  width: 100%;
  bottom: -20px;
  background-color: #e45447;
  margin: 0 auto;
  left: 0;
  right: 0;
  width: 100px;
}

.project-grid {
  display: grid;
  justify-content: center;
  margin: auto;
  grid-template-columns: 1fr 1fr;
  max-width: 1200px;
}
.project-grid > div {
  margin: 30px;
}
.projects-container {
  background-color: #f9f9ff;
  padding: 10px 0px;
}

@media screen and (max-width: 1000px) {
  .project-grid {
    grid-template-columns: 1fr;
  }
}
</style>
