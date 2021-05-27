<template>
  <div>
    <div class="slideshow-container">
      <div class="my-slides">
        <img class="slider-image" src="https://screenshot.click/07-55-y3mnx-mq9cc11.png">
      </div>
      <div class="my-slides">
        <img class="slider-image" src="https://screenshot.click/07-55-y3mnx-mq9cc22.png">
      </div>
      <div class="my-slides">
        <img class="slider-image" src="https://screenshot.click/07-55-y3mnx-mq9cc33.png">
      </div>
      <div class="three-dots">
        <span class="dot" @click="currentSlide(1)"></span>
        <span class="dot" @click="currentSlide(2)"></span>
        <span class="dot" @click="currentSlide(3)"></span>
      </div>
    </div>
  </div>
</template>

<script>
var slideIndex;
var slides = document.getElementsByClassName("my-slides");
var dots = document.getElementsByClassName("dot");

window.onload = function showFirst() {
  slides[0].style.display = "block";
  dots[0].className += " active";
}

function showSlides(n) {
  var i;
  if (n > slides.length) {slideIndex = 1}
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";
  }
  for (i = 0; i < dots.length; i++) {
    dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";
  dots[slideIndex-1].className += " active";
}

export default {
  name: "Slider",
  methods: {
    currentSlide(n) {
      showSlides(slideIndex = n);
    }
  },
}
</script>

<style scoped>
* {box-sizing:border-box}

.slideshow-container {
  margin-bottom: 40px;
}

.three-dots {
  text-align: center;
  margin-top: -40px;
}

.my-slides {
  display: none;
}

@keyframes slide {
  0% {opacity: 0}
  100% {opacity: 1}
}

.slider-image {
  width: 100%;
  animation: slide 1s ease-in;
}

.dot {
  cursor: pointer;
  height: 15px;
  width: 15px;
  margin: 0 2px;
  background-color: #bbb;
  border-radius: 50%;
  display: inline-block;
  transition: background-color 0.6s ease;
}

.active, .dot:hover {
  background-color: #717171;
}

@media (max-width: 640px) {
  .slider-image {
    height: 300px;
    object-fit: cover;
  }
}

</style>
