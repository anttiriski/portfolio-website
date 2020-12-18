<template>
  <div class="caption-container">
    <div class="captions">
      <span class="subheader">Hey! I am</span>
      <h1 class="name">Antti Riski !</h1>
      <vue-typed-js
        :typeSpeed="80"
        :backSpeed="40"
        :backDelay="2500"
        :loop="true"
        :strings="[
          'a Software Developer',
          'a Student',
          'an UI desinger',
          'a Snowboarder',
          'an Expert in the making',
        ]"
      >
        <h2>
          I'm
          <span class="typing"></span>
        </h2>
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
  margin-top: 64px;
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
