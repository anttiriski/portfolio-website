<template>
  <div class="about-section">
    <img class="about-image" src="../assets/about.jpg" alt="" />
    <AboutText />
  </div>
</template>

<script>
import AboutText from "../components/AboutText.vue";

export default {
  components: {
    AboutText,
  },
  name: "About",
};
</script>

<style>
.about-section {
  display: flex;
  max-width: 90rem;
  margin: auto;
  margin-bottom: 40px;
  padding: 0px 40px;
}
.about-image {
  max-width: 100%;
  max-height: 500px;
  outline: 10px solid #90acd1;
  outline-offset: -54px;
  border: 44px solid transparent;
  border-width: 0px 10px 0px 85px;
}

@media screen and (max-width: 1000px) {
  .about-image {
    display: none;
  }
}
</style>
