<template>
  <div class="hire-container">
    <h1 class="hire-title">HIRE ME</h1>
    <p class="hire-information">Take a risk, I promise it is worth it.</p>
    <p class="take-a-risk">Ota Riski</p>
  </div>
</template>

<script>
export default {
  name: "Hire",
};
</script>

<style>
.hire-container {
  height: 15rem;
  background-color: #e45447;
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 2rem;
}

.hire-title {
  font-size: 2.5rem;
  position: relative;
}

.hire-information {
  font-weight: 600;
  font-size: 1rem;
  margin: 2rem 0rem;
}

.take-a-risk {
  text-transform: uppercase;
  font-size: 12px;
}

.hire-title::after {
  position: absolute;
  content: "";
  height: 3px;
  width: 100px;
  bottom: -20px;
  background-color: white;
  margin: 0 auto;
  left: 0;
  right: 0;
}
</style>
