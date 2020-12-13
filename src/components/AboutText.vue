<template>
  <div class="about-text">
    <div>
      <h2 class="about-title">About Me</h2>
    </div>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. A eveniet maiores
      dolore. Facilis natus modi commodi voluptatum at ipsam id.
    </p>
    <ul class="about-info">
      <li><span>Name:</span><span>Antti Riski</span></li>
      <li><span>Date of birth:</span><span>January 16, 1999</span></li>
      <li><span>Email:</span><span>antti.riski@aalto.fi</span></li>
      <li><span>Phone</span><span>0403522771</span></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "AboutText",
};
</script>

<style>
.about-text {
  text-align: left;
  margin-left: 4rem;
}

.about-info {
  list-style: none;
  margin: 0;
  padding: 0;
}
.about-title {
  color: #222222;
  font-weight: 700;
  font-size: 45px;
  position: relative;
}
.about-title::after {
  position: absolute;
  content: "";
  height: 3px;
  width: 100px;
  bottom: -20px;
  background-color: #e45447;
  margin: 0 auto;
  left: 0;
}

.about-info li span:first-child {
  font-size: 16px;
  font-weight: 600;
  color: #222222;
  width: 130px;
}

.about-info li {
  display: flex;
  margin-top: 20px;
}
@media screen and (max-width: 1000px) {
  .about-title {
    text-align: center;
  }
  .about-text {
    margin: auto;
    text-align: center;
    max-width: 30rem;
  }
  .about-title::after {
    right: 0;
  }
  .about-info li {
    justify-content: center;
  }
}
</style>
