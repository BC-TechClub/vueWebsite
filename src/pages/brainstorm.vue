<template>
  <section>
    <div class="max-w-6xl mx-auto px-4 sm:px-6 relative background-container" style="min-height: calc(100vh + 600px)">
      <!-- Hero content -->
      <div class="relative pt-32 pb-10 md:pt-40 md:pb-16">

        <!-- Section header -->
        <VRow>
          <VCol cols="12" class="d-flex justify-center">
            <h1 class="headline" style="font-family: 'League Spartan', sans-serif; font-weight: bold; color: white">BRAINSTORM!</h1>
          </VCol>
          <VCol cols="12" class="d-flex justify-center">
            <div class="image-container">
              <!-- Update the width and height of the image for mobile -->
              <img :src="Lighting" class="static-image" style="width: 300px; height: 200px;"/>
            </div>
          </VCol>
            <div class="position-absolute bottom-0 start-50 translate-middle-x px-3 py-2 d-flex flex-column justify-content-center my-3" id="about_scroll" style="opacity: 1;">
              <small class="color-3">
                <strong>Learn More</strong>
              </small>
              <i class="bi bi-chevron-double-down d-flex justify-content-center color-3"></i>
            </div>
<!--          <div class="d-flex justify-center text-fade">-->
<!--            <div class="image container align-center">-->
<!--              <p class="align-center" style="font-family: 'League Spartan', sans-serif; font-weight: bolder; color: white; display: block; text-align: center">LEARN MORE</p>-->
<!--              <img :src="ScrollDown" class="scroll-down"/>-->
<!--            </div>-->
<!--          </div>-->
        </VRow>
        <VBtn color="white">Test</VBtn>
      </div>
    </div>
  </section>
</template>

<script setup>
import Lighting from '../assets/home/Tech_Club_New_Website.png'
import ScrollDown from '../assets/icons/Scroll down.png'
import {ref} from "vue";

const click = ref(false)
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=League+Spartan:wght@400;700&display=swap');


.image-container {
  position: relative;
  width: 300px; /* Set this to the size of your images */
  height: 200px; /* Set this to the size of your images */
}

.static-image {
  position: absolute;
  top: -30px;
  height: 200px;
  width: 300px;
  display: block;
  margin: auto;
  transition: transform 0.3s ease;
}

#about_scroll{
  transition-duration: 0.5s;
  background-color: transparent;
  border-radius: 30px;
  color: white;
}

#about_scroll:hover{
  background-color: rgba($color3, 0.2);
  cursor: pointer;
  background-color: #FF90C2;
}

@keyframes bobbing {
  0%, 100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-10px); /* This value controls the bobbing distance */
  }
}

.image-container:hover .static-image {
  animation: bobbing 0.5s ease-in-out infinite;
}

.scroll-down {
  height: 10px;
  width: 10px;
  display: block;
  margin: auto;

}

/* Add this media query to set the larger font size for desktop view */
@media screen and (min-width: 769px) {
  .headline {
    font-size: 100px; /* Adjust the font size for desktop view */
  }
}

/* Add this media query to set the smaller font size for mobile view */
@media screen and (max-width: 700px) {
  .headline {
    font-size: 60px; /* Adjust the font size for mobile view */
  }


}


</style>
