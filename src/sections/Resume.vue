<template>
  <div class="container">
    <div class="section-title">
      <h2>Resume</h2>
    </div>
    <div class="grid-container">
      <div class="Work card">
        <h1 class="card-header">Work</h1>
        <div class="workplace">
          <h3>Software Developer – Oikeat Oliot</h3>
        </div>
        <p class="paragraph">
          I worked as a junior
          <span class="highlight">designer-programmer</span> on an in-house
          development project. I learned a ton about UX, UI as well as essential
          skills in team-work and communications in organisations.
        </p>
      </div>
      <div class="Education card">
        <h1 class="card-header">Education</h1>
        <div class="school">
          <h3>Aalto-university - Information networks</h3>
          <p class="highlight">Master of science student</p>
          <p class="year">2019 - 2025</p>
        </div>
      </div>
      <div class="Expertises card">
        <h1 class="card-header">Expertises</h1>
        <div class="skills">
          <p>jee</p>
          <p>jee</p>
          <p>jee</p>
          <p>jee</p>
          <p>jee</p>
          <p>jee</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Resume",
};
</script>

<style>
.section-title h2 {
  color: #222222;
  font-weight: 700;
  font-size: 45px;
  line-height: 50px;
  position: relative;
  margin-bottom: 60px;
}
.section-title h2::after {
  position: absolute;
  content: "";
  height: 3px;
  width: 100%;
  bottom: -20px;
  background-color: #e45447;
  margin: 0 auto;
  left: 0;
  right: 0;
  width: 100px;
}
.grid-container {
  display: grid;
  grid-template-columns: 0.3fr 1fr 1fr 1fr 1fr 0.3fr;
  grid-template-rows: 0.6fr 0.4fr 1fr 0.3fr;
  gap: 20px 20px;
  grid-template-areas:
    ". Work Work Education Education ."
    ". Work Work Education Education ."
    ". Expertises Expertises Expertises Expertises ."
    ". Expertises Expertises Expertises Expertises .";
}
.card {
  text-align: left;
  padding: 2rem;
  border-radius: 10px;
  box-shadow: 0 8px 10px 0px rgba(0, 0, 0, 0.35);
}
.Work {
  grid-area: Work;
}
.Education {
  grid-area: Education;
}
.Expertises {
  grid-area: Expertises;
}
.workplace {
  display: flex;
  justify-content: left;
  align-items: center;
}
.oliot {
  margin-left: 5px;
}
.highlight {
  color: #e45447;
  font-weight: 700;
}
.paragraph {
  text-align: left;
}
.card-header {
  margin: 0;
}
.year {
  font-size: 20px;
}
</style>
