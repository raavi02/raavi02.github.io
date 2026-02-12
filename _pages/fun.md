---
layout: splash
title: "My Space"
permalink: /fun/
---

<div class="carousel">
  <div class="carousel-inner">
    <div class="carousel-item">
      <img src="/files/bungee-jumping.gif" alt="Your GIF Description">
      <p class="carousel-caption">190 ft bungee jumping at world's highest bungee jumping site.</p>
    </div>
    <div class="carousel-item">
      <img src="/files/hampta-pass.jpg" alt="Image 1">
      <p class="carousel-caption">Hampta pass top@14k feet. Took 3 days to reach.</p>
    </div>
    <div class="carousel-item">
      <img src="/files/tip2tip.png" alt="Image 2">
      <p class="carousel-caption">Tip-to-tip across Manhattan: 14 miles (26 km) in one epic walk!</p>
    </div>
    <div class="carousel-item">
      <img src="/files/car-trip.jpg" alt="Car Trip">
      <p class="carousel-caption">25+ states and 8k miles in 21 days</p>
    </div>
    <div class="carousel-item">
      <img src="/files/kuari-pass-2.jpg" alt="Kuari Pass">
      <p class="carousel-caption">Kuari pass trek@12.5 feet</p>
    </div>
  </div>
  <button class="carousel-control prev" onclick="moveCarousel(-1)">&#10094;</button>
  <button class="carousel-control next" onclick="moveCarousel(1)">&#10095;</button>
</div>

<script>
let currentSlide = 0;
const slides = document.querySelectorAll('.carousel-item');

function moveCarousel(n) {
  currentSlide += n;
  if (currentSlide >= slides.length) {currentSlide = 0}
  if (currentSlide < 0) {currentSlide = slides.length - 1}
  slides.forEach(slide => slide.style.display = "none");
  slides[currentSlide].style.display = "block";
}

moveCarousel(0);
</script>

<style>
.carousel {
  position: relative;
  width: 100vw;
  left: 50%;
  right: 50%;
  margin-left: -50vw;
  margin-right: -50vw;
}
.carousel-item {
  display: none;
  text-align: center;
  background-color: #000; /* Optional: black background for images that don't fill screen */
}
.carousel-item img {
  width: 100%;
  height: auto;
  max-height: 90vh; /* Prevent scrolling on most screens */
  object-fit: contain;
}
.carousel-caption {
  text-align: center;
  margin-top: 10px;
  color: #fff; /* Ensure caption is visible if background is dark, or add background to caption */
  background: rgba(0, 0, 0, 0.5); /* Semi-transparent background for readability */
  padding: 10px;
  position: absolute;
  bottom: 0;
  width: 100%;
}
.carousel-control {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background: rgba(0,0,0,0.5);
  color: white;
  border: none;
  padding: 10px;
  cursor: pointer;
  z-index: 10;
}
.prev {left: 20px;}
.next {right: 20px;}
</style>
