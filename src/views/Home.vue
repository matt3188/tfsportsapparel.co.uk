<template>
  <div class="home">
    <b-carousel
      :arrow="false"
      :has-drag="false"
      :pause-hover="false"
      :indicator="false"
      :interval="6000"
    >
      <b-carousel-item v-for="(image, i) in images" :key="i">
        <span class="image" :style="`background-image: url(${image})`"> </span>
      </b-carousel-item>
    </b-carousel>
    <div class="logo-container">
      <TheLogo />

      <!-- <h1 class="heading is-size-3 mt-5">
        OUR NEW WEBSITE IS<br />LAUNCHING SOON
      </h1> -->

      <!-- <p class="mt-5">OUR NEW SITE IS</p>
      <h1 class="heading is-size-3">COMING SOON</h1>

      <h1 class="heading is-size-3 mt-5">
        WE ARE CURRENTLY WORKING<br />
        ON OUR NEW WEBSITE
      </h1> -->

      <h1 class="heading is-size-3 mt-5">COMING SOON</h1>
      <p>WE ARE CURRENTLY WORKING ON OUR NEW WEBSITE</p>
    </div>
  </div>
</template>

<script>
import TheLogo from '@/components/TheLogo'
import image1 from '@/assets/images/West_Ham.MR_094.jpg'
import image2 from '@/assets/images/West_Ham.MR_078.jpg'

export default {
  name: 'Home',
  components: { TheLogo },
  data() {
    return {
      images: [image1, image2]
    }
  }
}
</script>

<style lang="scss" scoped>
.home {
  overflow: hidden;
}
.logo-container {
  align-items: center;
  bottom: 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  left: 0;
  margin: auto;
  position: absolute;
  right: 0;
  top: 0;

  .logo {
    width: 350px;
  }
}

.carousel-item,
.carousel-item:after {
  position: fixed;
  width: 100%;
  height: 100%;
  top: 0px;
  left: 0px;
  z-index: 0;
}

.carousel-item:after {
  content: '';
  background: rgba(12, 17, 45, 50%);
}

.section {
  position: relative;
  background-size: cover;
  background-position: center;
}
.slide {
  background-size: cover;
  background-position: center;
}
.image {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0px;
  left: 0px;
  color: transparent;
  background-size: cover;
  background-position: 50% 50%;
  background-repeat: none;
}
.heading {
  font-family: 'Roboto', sans-serif;
  font-weight: 500;
  color: #fff;
  position: relative;
  text-align: center;
}
</style>
