<template>
  <div>
    <div v-if="showModal" class="modal">
      <div class="modal-mask" @click="closeModal"></div>
      <div class="modal-content">
        <span @click="closeModal" class="modal-exit">&#10005;</span>
        <h2 class="modal-project-name">{{ project.name }}</h2>
        <img
          class="modal-image"
          :src="require(`@/assets/${project.image_source}`)"
          alt="Project image"
        />
        <div class="modal-information">
          <p>
            <span class="bold">Description: </span>
            {{ project.description }}
          </p>
          <p>
            <span class="bold">Learned about: </span>
            {{ project.learned }}
          </p>
        </div>
        <div class="project-buttons">
          <a
            :class="project.demo ? 'button' : 'no-demo'"
            target="blank"
            :href="project.demo"
          >
            Live demo
          </a>
          <a
            :class="project.source ? 'button' : 'no-demo'"
            target="blank"
            :href="project.source"
          >
            Source Code
          </a>
        </div>
      </div>
    </div>

    <div class="project-content">
      <div class="image-zoom">
        <img
          class="project-image"
          :src="require(`@/assets/${project.image_source}`)"
          alt="Project image"
          @click="showModal = true"
        />
      </div>
      <div class="project-information">
        <p @click="showModal = true" class="project-title">
          {{ project.name }}
        </p>
        <div class="project-links">
          <GithubIcon v-if="project.source" :link="project.source" :size="24" />
          <LinkToSource v-if="project.demo" :link="project.demo" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import GithubIcon from "../icons/GithubIcon";
import LinkToSource from "../icons/LinkToSource";

export default {
  name: "ProjectModal",
  data() {
    return {
      showModal: false,
      image: {
        backgroundImage:
          "url(" + require(`@/assets/${this.project.image_source}`) + ")",
      },
    };
  },
  props: {
    project: Object,
  },
  methods: {
    closeModal: function() {
      this.showModal = false;
    },
  },
  components: {
    GithubIcon,
    LinkToSource,
  },
};
</script>

<style>
.modal-mask {
  position: fixed;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgb(0, 0, 0, 0.3);
  cursor: pointer;
  z-index: 5;
}

.modal-content {
  position: fixed;
  max-width: 1200px;
  width: 70%;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  padding: 20px;
  background-color: white;
  border-radius: 5px;
  z-index: 10;
}

.modal-information {
  text-align: left;
  max-width: 50rem;
  margin: auto;
}

.modal-exit {
  font-size: 30px;
  position: absolute;
  right: 0;
  margin-right: 10px;
  cursor: pointer;
}

.project-image {
  max-width: 100%;
  display: block;
  border-radius: 10px;
  transition: 0.3s;
}

.image-zoom {
  overflow: hidden;
}

.project-content {
  cursor: pointer;
  position: relative;
  display: flex;
  flex-direction: column;
  box-shadow: 0 8px 10px 0px rgba(0, 0, 0, 0.35);
  border-radius: 10px;
  transition: 0.3s;
  background-color: white;
  height: 100%;
  flex: 1;
}

.project-content:hover .project-information {
  background-color: #e45447;
  border-radius: 0px 0px 10px 10px;
  color: white;
}

.project-content:hover .project-links a {
  fill: white;
}

.project-content:hover .project-image {
  scale: 1.05;
}

.modal-image {
  max-width: 1000px;
  width: 100%;
}

.bold {
  font-weight: 700;
}

.button,
.no-demo {
  text-decoration: none;
  padding: 10px 20px;
  margin: 0px 5px;
  border: 2px solid;
  border-radius: 5px;
  color: black;
}

.project-buttons {
  display: flex;
  justify-content: center;
}

.button:hover {
  color: #e45447;
  border: 2px solid #e45447;
}

.project-title {
  font-weight: 700;
  font-size: 23px;
  text-align: left;
  position: relative;
}

.modal-project-name {
  position: relative;
}

.modal-project-name::after {
  position: absolute;
  content: "";
  height: 3px;
  width: 100%;
  bottom: -13px;
  background-color: #e45447;
  margin: 0 auto;
  left: 0;
  right: 0;
  width: 100px;
}

.project-information {
  display: flex;
  justify-content: space-between;
  padding: 0rem 2rem;
  color: #e45447;
  flex: 1;
  align-items: center;
  transition: 0.3s;
}

.project-links {
  display: flex;
  align-items: center;
  transition: 0.3s;
}

.project-links a {
  margin: 0 0.4rem;
}

.no-demo {
  color: #a9a9a9;
}
</style>
