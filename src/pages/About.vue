<template>
  <q-page>
    <div class="w-100 about-wrapper">
      <div class="about-heading">About Us</div>
      <div class="about-content">
        Welcome to our platform, where the spirit of adventure knows no bounds!
        We are a passionate team of adventure enthusiasts dedicated to providing
        thrill-seekers with a revolutionary platform for discovering, booking,
        and experiencing extraordinary adventures across the globe. Our mission
        is to empower individuals to embrace their inner adventurers and explore
        the world with exhilaration, wonder, and unforgettable memories.
      </div>
      <div class="about-sub-heading">Unleashing the Adventurer Within</div>
      <div class="about-content">
        At our core, we believe that life is meant to be lived to the fullest,
        and that means embracing thrilling experiences that challenge and excite
        us. Whether you're a seasoned adrenaline junkie or someone seeking to
        step out of your comfort zone, our platform offers an extensive array of
        adventure sports and activities to suit all levels of experience. From
        heart-pounding skydiving and white-water rafting to serene hiking
        expeditions and everything in between, there's something to cater to
        every adventurer's desires.
      </div>
    </div>
  </q-page>
</template>

<script>
export default {};
</script>

<style>
.about-wrapper {
  /* background-color: #263238; */
  min-height: 100vh;
  width: 100%;
  padding: 60px 100px 200px;
  background-image: url('../assets/about-bg.png');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: bottom;
}
.about-heading {
  font-family: 'Ubuntu';
  font-style: normal;
  font-weight: 600;
  font-size: 50px;
}
.about-content {
  padding: 20px 0;
  font-size: 18px;
  font-weight: 400;
  font-style: normal;
  font-family: 'Poppins';
}
.about-sub-heading {
  font-family: 'Ubuntu';
  font-style: normal;
  font-weight: 500;
  font-size: 30px;
}
@media (max-width: 900px) {
  .about-wrapper {
    padding: 20px;
  }
  .about-heading {
    font-size: 30px;
  }
  .about-sub-heading {
    font-size: 20px;
  }
  .about-content {
    font-size: 16px;
  }
}
</style>
