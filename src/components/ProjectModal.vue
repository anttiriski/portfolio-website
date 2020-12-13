<template>
  <div>
    <div v-if="showModal" class="modal">
      <div class="modal-mask" @click="closeModal"></div>
      <div class="modal-content">
        <span @click="closeModal" class="exit">&#10005;</span>
        <h2>{{ project.name }}</h2>
        <div class="image">
          <img
            :src="require(`@/assets/${project.image_source}`)"
            alt="Project image"
          />
        </div>
        <p><span class="bold">Made with:</span> {{ project.tech }}</p>
        <p><span class="bold">Learned about:</span> {{ project.learned }}</p>
        <div class="project-buttons">
          <a class="button" target="blank" :href="project.demo">Live demo</a>
          <a class="button" target="blank" :href="project.source"
            >Source Code</a
          >
        </div>
      </div>
    </div>
    <div class="project-content">
      <img
        class="project-image"
        :src="require(`@/assets/${project.image_source}`)"
        alt="Project image"
        @click="showModal = true"
      />
      <div class="project-information">
        <p @click="showModal = true" class="project-title">
          {{ project.name }}
        </p>
        <div class="project-links">
          <a target="blanc" :href="project.source"
            ><svg
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 24 24"
            >
              <path
                d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"
              /></svg
          ></a>
          <a target="blanc" :href="project.demo"
            ><svg
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 24 24"
            >
              <path
                d="M6.188 8.719c.439-.439.926-.801 1.444-1.087 2.887-1.591 6.589-.745 8.445 2.069l-2.246 2.245c-.644-1.469-2.243-2.305-3.834-1.949-.599.134-1.168.433-1.633.898l-4.304 4.306c-1.307 1.307-1.307 3.433 0 4.74 1.307 1.307 3.433 1.307 4.74 0l1.327-1.327c1.207.479 2.501.67 3.779.575l-2.929 2.929c-2.511 2.511-6.582 2.511-9.093 0s-2.511-6.582 0-9.093l4.304-4.306zm6.836-6.836l-2.929 2.929c1.277-.096 2.572.096 3.779.574l1.326-1.326c1.307-1.307 3.433-1.307 4.74 0 1.307 1.307 1.307 3.433 0 4.74l-4.305 4.305c-1.311 1.311-3.44 1.3-4.74 0-.303-.303-.564-.68-.727-1.051l-2.246 2.245c.236.358.481.667.796.982.812.812 1.846 1.417 3.036 1.704 1.542.371 3.194.166 4.613-.617.518-.286 1.005-.648 1.444-1.087l4.304-4.305c2.512-2.511 2.512-6.582.001-9.093-2.511-2.51-6.581-2.51-9.092 0z"
              /></svg
          ></a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
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
  background-color: white;
  border-radius: 5px;
  z-index: 10;
}
.exit {
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
}

.project-content {
  cursor: pointer;
  position: relative;
  box-shadow: 0 8px 10px 0px rgba(0, 0, 0, 0.35);
  border-radius: 10px;
  transition: 0.3s;
  background-color: white;
}

.project-content:hover {
  transform: translateY(-3px);
}

.image img {
  max-width: 1000px;
  width: 100%;
}
.bold {
  font-weight: 700;
}
.button {
  text-decoration: none;
  padding: 10px 20px;
  margin: 10px 20px;
  border: 2px solid;
  border-radius: 5px;
  color: black;
}
.project-buttons {
  margin: 30px 0px;
}

.button:hover {
  color: #e45447;
  border: 2px solid #e45447;
}

.project-title {
  font-weight: 700;
  font-size: 23px;
}
.project-information {
  display: flex;
  justify-content: space-between;
  margin: 0rem 2rem;
  color: #e45447;
}

.project-links {
  display: flex;
  align-items: center;
}
.project-links a {
  margin: 0 0.4rem;
}
</style>
