<template>
  <div class="footer">
    <span>Thanks for reading<b class="heart">&lt;3</b></span>
    <div class="footer-links">
      <GithubIcon :link="linkToGithub" :size="40" />
      <LinkIcon :link="linkToLinkedIn" />
    </div>
  </div>
</template>

<script>
import GithubIcon from "../icons/GithubIcon";
import LinkIcon from "../icons/LinkedInIcon";

export default {
  name: "Footer",
  data() {
    return {
      linkToGithub: "https://github.com/anttiriski",
      linkToLinkedIn: "https://www.linkedin.com/in/antti-riski-b4637319a/",
    };
  },
  components: {
    GithubIcon,
    LinkIcon,
  },
};
</script>

<style>
.footer {
  height: 20rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: #f9f9ff;
}

.footer-links {
  margin: 2rem 0rem;
  display: flex;
  width: 10rem;
  justify-content: space-around;
}

.heart {
  margin-left: 0.5rem;
}
</style>
