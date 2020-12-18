<template>
  <div class="resume-container">
    <div class="section-title">
      <h2>Resume</h2>
    </div>
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
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Omnis
          laboriosam cum voluptatum esse placeat possimus saepe incidunt
          provident facere aliquam ex, modi accusantium et labore quas eum sint.
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
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Omnis
          laboriosam cum voluptatum esse placeat possimus saepe incidunt
          provident facere aliquam ex, modi accusantium et labore quas eum sint.
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

.highlight {
  color: #e45447;
  font-weight: 700;
}

.paragraph {
  max-width: 400px;
  margin: auto;
}

.card {
  max-width: 800px;
  margin: auto;
}

.card:last-child {
  margin-bottom: 50px;
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
}

.resume-container {
  padding: 0rem 2rem;
}
</style>
