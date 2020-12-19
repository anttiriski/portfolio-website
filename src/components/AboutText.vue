<template>
  <div class="about">
    <h2 class="about-title">About Me</h2>
    <div class="about-text">
      <div>
        <p class="about-p">
          I want to create something that really affects other people, and
          create it in clean, beautiful, interactive, minimalistic, responsive &
          user friendly way. I want to help others, if they need it; I really
          have the joy of giving.
        </p>
        <ul class="about-info">
          <li><span>Name:</span><span>Antti Riski</span></li>
          <li><span>Date of birth:</span><span>January 16, 1999</span></li>
          <li><span>Email:</span><span>antti.riski@aalto.fi</span></li>
          <li><span>Phone</span><span>040 3522771</span></li>
        </ul>
      </div>
      <img id="img" src="../assets/about.jpg" alt="about-image" />
    </div>
  </div>
</template>

<script>
export default {
  name: "AboutText",
};
</script>

<style>
.about {
  display: flex column;
  padding-left: 100px;
}
.about-text {
  display: flex;
  text-align: left;
}
.about-info {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: column;
  font-size: 1.1rem;
}

#img {
  max-height: 300px;
  display: none;
  margin: 20px;
}
.about-title {
  font-weight: 700;
  font-size: 2.75rem;
  position: relative;
  text-align: left;
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
  .about-title::after {
    right: 0;
  }
  .about {
    padding: 0;
  }
  #img {
    display: block;
  }
}
@media screen and (max-width: 550px) {
  #img {
    display: none;
  }
}
</style>
