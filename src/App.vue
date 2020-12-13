<template>
  <div id="app">
    <Navigation />
    <Home id="Home" />
    <About id="About" />
    <Projects id="Projects" />
    <Resume id="Resume" />
    <Footer />
  </div>
</template>

<script>
import Home from "./sections/Home";
import Navigation from "./components/Navigation";
import About from "./sections/About";
import Resume from "./sections/Resume";
import Projects from "./sections/Projects";
import Footer from "./sections/Footer";

export default {
  name: "App",
  components: {
    Home,
    Navigation,
    About,
    Resume,
    Projects,
    Footer,
  },
};
</script>

<style>
html,
body {
  padding: 0px;
  margin: 0px;
}
#app {
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
