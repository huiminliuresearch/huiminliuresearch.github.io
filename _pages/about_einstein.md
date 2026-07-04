<div class="laszlo-page-layout">
  <div class="laszlo-page-text">
    <p>Laszlo is a four-year-old domestic medium-hair cat and the major research supporter behind the scenes. He provides emotional support, clingy companionship, and a daily role model of bravery and scrappy determination.</p>

    <p>His notable achievements include turning the screen of a brand-new MacBook Pro — the newest model of that year — black with one bite, and chewing through expensive charging cables while kindly leaving the cheap ones intact. These contributions have strongly motivated me to work harder and provide him with an even better life.</p>
  </div>

  <div class="laszlo-slideshow" data-interval="5000" aria-label="Laszlo photo slideshow">
    <div class="laszlo-slide is-active">
      <img src="/assets/img/cat.jpg" alt="Laszlo in a paper bag">
    </div>
    <div class="laszlo-slide">
      <img src="/assets/img/laszlo-gallery-01.jpg" alt="Laszlo resting">
    </div>
    <div class="laszlo-slide">
      <img src="/assets/img/laszlo-gallery-02.jpg" alt="Laszlo looking at the camera">
    </div>
    <div class="laszlo-slide">
      <img src="/assets/img/laszlo-gallery-03.jpg" alt="Laszlo relaxing">
    </div>
    <div class="laszlo-slide">
      <img src="/assets/img/laszlo-gallery-04.jpg" alt="Laszlo as a kitten">
    </div>
    <div class="laszlo-slide">
      <img src="/assets/img/laszlo-gallery-05.jpg" alt="Laszlo close-up">
    </div>
  </div>
</div>

<script>
  document.addEventListener("DOMContentLoaded", function () {
    document.querySelectorAll(".laszlo-slideshow").forEach(function (slideshow) {
      const slides = Array.from(slideshow.querySelectorAll(".laszlo-slide"));
      const interval = Number(slideshow.dataset.interval || 5000);
      let activeIndex = 0;

      function showSlide(index) {
        activeIndex = index;
        slides.forEach(function (slide, slideIndex) {
          slide.classList.toggle("is-active", slideIndex === activeIndex);
        });
      }

      window.setInterval(function () {
        showSlide((activeIndex + 1) % slides.length);
      }, interval);
    });
  });
</script>
