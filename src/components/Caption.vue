<template>
  <div class="caption-container">
    <div class="captions">
      <span class="subheader">Hey! I am</span>
      <h1 class="caption-header">Antti Riski !</h1>
      <vue-typed-js
        :typeSpeed="80"
        :backSpeed="40"
        :backDelay="2500"
        :loop="true"
        :strings="[
          'a Software Developer',
          'a Student',
          'an UI desinger',
          'an Expert in the making',
        ]"
      >
        <h2>I'm <span class="typing"></span></h2>
      </vue-typed-js>
      <p class="caption-text">
        I'm everything that is said above, and beyond. I prefer active
        lifestyle; hangout with friends, play games, try something new or
        sometimes just pop a beer and watch youtube. I'm just a normal guy, with
        a sense of humor and an eye for UI/UX.
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

.caption-header {
  font-size: 3.5rem;
  margin: 0;
}

.subheader {
  font-size: 1.25rem;
  text-transform: uppercase;
}

.typing {
  color: #e45447;
  font-size: 1.6rem;
}

.caption-container {
  margin: 2.6rem;
}
</style>
