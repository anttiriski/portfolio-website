<template>
  <div class="resume-container">
    <h2 class="section-title">Resume</h2>
    <div class="card">
      <h2 class="card-title">Education</h2>
      <div class="card-content">
        <h4>2019 - 20??</h4>
        <h2>
          <span class="highlight">Master of Science student</span>, Information
          networks
        </h2>
        <h4>Aalto-university</h4>
        <p>
          I'm in love with this study program. Information networks connects
          technology, business & people together. I very much enjoy my time
          here, especially our guild Athene. One of our students made a very
          good
          <a
            href="https://www.youtube.com/watch?v=cEQvHy4Tevk&ab_channel=AaltoInformaatioverkostot"
            target="_blank"
            class="highlight"
            >video</a
          >
          about Athene, go check it out!! (thanks Iida)
        </p>
      </div>
    </div>
    <div class="card">
      <h2 class="card-title">Work Experience</h2>
      <div class="card-content">
        <h4>Summer job 2020</h4>
        <h2 class="highlight">Software developer</h2>
        <h4>Oikeat Oliot Oy</h4>
        <p>
          I worked as a junior designer-programmer on an in-house development
          project. Our team developed a prototype of a smart office remote
          control for a portable device.
        </p>
        <p>
          During the summer, I really learned a lot about UI desing, UX desing
          and front-end programming, as well as essential skills in team-work
          and communications in organisation culture.
        </p>
      </div>
    </div>
    <div class="card">
      <h2 class="card-title">Favorite animal</h2>
      <div class="card-content">
        <h4>Since 2019</h4>
        <h2 class="highlight">Debugging duck</h2>
        <h4>Location: my desk</h4>
        <p>This duckn't need any explanations, does it?</p>
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
.section-title {
  color: #222222;
  font-weight: 700;
  font-size: 45px;
  line-height: 50px;
  position: relative;
  margin: 0 0 2rem 0;
}
.section-title::after {
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

.highlight {
  color: #e45447;
  font-weight: 700;
  text-decoration: none;
}

.card {
  max-width: 800px;
  margin: auto;
}

.card-title {
  text-align: left;
  position: relative;
}

.card-content {
  text-align: left;
  padding: 2rem;
  border-radius: 10px;
  margin-left: 40px;
  background-color: #f9f9ff;
  transition: 0.3s;
}

.resume-container {
  padding: 2rem;
}

@media screen and (max-width: 600px) {
  .card-content {
    padding: 1rem;
  }
}
</style>
