<template>
  <div class="navigation-bar">
    <div class="logo"></div>
    <ul class="navigation">
      <li><a class="nav-link" href="#Home">Home</a></li>
      <li><a class="nav-link" href="#About">About</a></li>
      <li><a class="nav-link" href="#Resume">Resume</a></li>
      <li><a class="nav-link" href="#Projects">Projects</a></li>
      <li><a class="nav-link" href="#Contact">Contact</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Navigation",
};
</script>

<style>
.navigation-bar {
  background-color: #f9f9ff;
}

.navigation {
  list-style: none;
  display: flex;
  align-items: center;
  margin: 0px 60px 0px 0px;
  justify-content: flex-end;
  height: 4rem;
}

.navigation > li {
  margin: 0px 20px;
}

.nav-link {
  text-decoration: none;
  color: black;
}
</style>
