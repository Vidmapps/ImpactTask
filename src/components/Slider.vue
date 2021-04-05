<template>
  <div>
    <div class="slideshow-container">
      <div class="my-slides fade">
        <img class="slider-image" src="https://screenshot.click/05-39-4ywuy-eq9v6.png">
      </div>
      <!--<div class="my-slides fade">
        <img class="slider-image" src="https://screenshot.click/05-39-4ywuy-eq9v62.png">
      </div>
      <div class="my-slides fade">
        <img class="slider-image" src="https://screenshot.click/05-39-4ywuy-eq9v60.png">
      </div>-->
    </div>
    <br>
    <div style="text-align:center">
      <span class="dot" @click="currentSlide(1)"></span>
      <span class="dot" @click="currentSlide(2)"></span>
      <span class="dot" @click="currentSlide(3)"></span>
    </div>
  </div>
</template>

<script>
var slideIndex = 1;

function showSlides(n) {
  var i;
  var slides = document.getElementsByClassName("my-slides");
  var dots = document.getElementsByClassName("dot");
  if (n > slides.length) {slideIndex = 1}
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
    slides[i].style.display = "block"; // none
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
  }
}
</script>

<style scoped>
* {box-sizing:border-box}

.slideshow-container {
  position: relative;
  margin: auto;
}

.my-slides {
  display: none;
}

.slider-image {
  width: 100%;
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

.fade {
  -webkit-animation-name: fade;
  -webkit-animation-duration: 1.5s;
  animation-name: fade;
  animation-duration: 1.5s;
}

@-webkit-keyframes fade {
  from {opacity: .4}
  to {opacity: 1}
}

@keyframes fade {
  from {opacity: .4}
  to {opacity: 1}
}
</style>
