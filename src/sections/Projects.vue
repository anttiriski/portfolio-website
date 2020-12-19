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
.projects-container {
  background-color: #f9f9ff;
  padding: 3rem 0rem;
}

.project-header {
  font-weight: 700;
  font-size: 2.75rem;
  position: relative;
  margin-top: 0;
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
  grid-template-columns: fit-content(25%) fit-content(25%) fit-content(25%);
  grid-gap: 1rem;
}

@media screen and (max-width: 1575px) {
  .project-grid {
    grid-template-columns: fit-content(40%) fit-content(40%);
  }
}

@media screen and (max-width: 1000px) {
  .project-grid {
    grid-template-columns: fit-content(85%);
  }
}
</style>
