---
layout: page
title: "My Space"
permalink: /fun/
---

[//]: # (<center>)

[//]: # (  <img src="/files/myVisitedPlaces.gif" alt="" )

[//]: # (width="50%">)

[//]: # (</center>)

<!-- <center>
  <img src="/files/myVisitedPlaces.gif" alt="Your GIF Description" width="50%">
</center>
<center>
    Countries I have visited so far. 
</center> -->

<center>
    <h3 class="carousel-heading">Some people dance. Some people sing. I do adventure sports [WiP].</h3>
</center>

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
  max-width: 600px;
  margin: auto;
}
.carousel-item {
  display: none;
}
.carousel-item img {
  width: 100%;
  height: 400px; /* Fixed height */
  object-fit: cover;
  object-position: center;
}
.carousel-caption {
  text-align: center;
  margin-top: 10px;
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
}
.prev {left: 0;}
.next {right: 0;}
</style>

<center>
Apart from this, I like reading books (Agatha Christie's my favorite) and solving jigsaw puzzles.
</center>
