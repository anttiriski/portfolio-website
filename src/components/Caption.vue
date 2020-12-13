<template>
  <div class="caption-container">
    <div class="captions">
      <span class="subheader">Hey! I am</span>
      <h1 class="name">Antti Riski!</h1>
      <vue-typed-js
        :typeSpeed="80"
        :backSpeed="40"
        :backDelay="2500"
        :loop="true"
        :strings="['Software Developer', 'Student', 'UI desinger', '']"
      >
        <h2>
          I'm a
          <span class="typing"></span>
        </h2>
      </vue-typed-js>
      <p class="caption-text">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas animi,
        voluptates sapiente distinctio molestias eveniet iusto! Expedita alias
        dolore in.
      </p>
    </div>
  </div>
</template>

<script>
import Vue from "vue";
import VueTypedJs from "vue-typed-js";

Vue.use(VueTypedJs);
export default {
  name: "Caption",
};
</script>

<style>
.captions {
  text-align: left;
  max-width: 40rem;
}

.name {
  font-size: 4rem;
  margin: 0;
}

.subheader {
  font-size: 1.6rem;
  text-transform: uppercase;
}

.typing {
  color: #e45447;
  font-size: 30px;
  margin-bottom: 30px;
}
.caption-container {
  margin: 3rem;
}
</style>
