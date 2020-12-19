<template>
  <div v-if="showMenu" id="navbar">
    <div class="logo"></div>
    <ul class="navigation">
      <li><a class="nav-link" href="#Home">Home</a></li>
      <li><a class="nav-link" href="#About">About</a></li>
      <li><a class="nav-link" href="#Projects">Projects</a></li>
      <li><a class="nav-link" href="#Resume">Resume</a></li>
    </ul>
  </div>
  <div v-else id="navbar">
    <div class="menuContainer" @click="handleClick">
      <div class="bar1"></div>
      <div class="bar2"></div>
      <div class="bar3"></div>
    </div>
    <div v-if="showDropdown">
      <ul class="mobile-navigation">
        <li>
          <a @click="handleClick" class="nav-link" href="#Home">Home</a>
        </li>
        <li>
          <a @click="handleClick" class="nav-link" href="#About">About</a>
        </li>
        <li>
          <a @click="handleClick" class="nav-link" href="#Projects">Projects</a>
        </li>
        <li>
          <a @click="handleClick" class="nav-link" href="#Resume">Resume</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
var prevScrollpos = window.pageYOffset;
window.onscroll = function() {
  var currentScrollPos = window.pageYOffset;
  if (prevScrollpos > currentScrollPos) {
    document.getElementById("navbar").style.top = "0";
  } else {
    document.getElementById("navbar").style.top = "-64px";
  }
  prevScrollpos = currentScrollPos;
};

export default {
  name: "Navigation",
  data() {
    return {
      showMenu: window.innerWidth > 1000,
      showDropdown: false,
    };
  },
  created() {
    window.addEventListener("resize", (event) => {
      this.showMenu = event.target.innerWidth > 1000;
    });
  },
  methods: {
    handleClick() {
      const container = document.getElementsByClassName("menuContainer")[0];
      container.classList.toggle("change");
      this.showDropdown = !this.showDropdown;
    },
  },
};
</script>

<style>
#navbar {
  background-color: #f9f9ff;
  position: fixed;
  width: 100%;
  z-index: 5;
  transition: 0.4s;
}

.navigation {
  list-style: none;
  display: flex;
  align-items: center;
  margin: 0 4rem 0 0;
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

.bar1,
.bar2,
.bar3 {
  width: 34px;
  height: 5px;
  background-color: #333;
  margin: 3px 0;
  transition: 0.4s;
}

.menuContainer {
  cursor: pointer;
  margin: 10px 20px;
  z-index: 1;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
}

.change .bar1 {
  transform: rotate(-45deg) translate(-8px, 7px);
}

.change .bar2 {
  opacity: 0;
}

.change .bar3 {
  transform: rotate(45deg) translate(-8px, -8px);
}

.mobile-navigation {
  list-style: none;
  margin: 0;
  padding: 0;
  padding-bottom: 20px;
  box-shadow: 0 6px 5px 0px rgba(0, 0, 0, 0.35);
  height: 100vh;
}

.mobile-navigation li {
  font-size: 1.5rem;
  padding: 20px 0px;
}
</style>
