<template>
  <div class="row">
    <div class="caption">
      <Caption />
      <div class="animation">
        <img src="../assets/circle.png" alt="" />
      </div>
    </div>
    <img class="about-img" src="../assets/landing_picture.jpg" alt="" />
  </div>
</template>

<script>
import Caption from "../components/Caption";

export default {
  name: "Home",
  components: {
    Caption,
  },
};
</script>

<style>
.row {
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #f9f9ff;
}
@media screen and (max-width: 1000px) {
  .row .about-img {
    display: none;
  }
}
.caption {
  position: relative;
}

.animation {
  position: absolute;
  top: 0;
  right: 0;
  margin-right: 100px;
  backface-visibility: hidden;
  animation: jumping 9s ease-in-out 2s infinite alternate;
  animation-delay: 1s;
  transition: all 15s ease 2s;
  user-select: none;
}
@keyframes jumping {
  20% {
    transform: translateY(20px) scale(0.8);
  }
  40% {
    transform: translate(10px, 30px) scale(0.6);
  }
  60% {
    transform: translate(-30px, -40px) scale(0.7);
  }
  80% {
    transform: translate(-20wpx, 40px) scale(0.6);
  }
  100% {
    transform: translate(20px, -10px) scale(0.8);
  }
}
</style>
