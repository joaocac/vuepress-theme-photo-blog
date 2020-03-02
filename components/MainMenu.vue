<template>
  <!-- ***** Main Menu Area Start ***** -->
  <div class="mainMenu d-flex align-items-center justify-content-between">
    <!-- Close Icon -->
    <div class="closeIcon">
      <i class="ti-close" aria-hidden="true"></i>
    </div>
    <!-- Logo Area -->
    <div class="logo-area">
      <a href="index.html">T.</a>
    </div>
    <!-- Nav -->
    <div class="sonarNav wow fadeInUp" data-wow-delay="1s">
      <nav>
        <ul>
          <li class="nav-item active">
            <a class="nav-link" href="index.html">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="about-me.html">About Me</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="services.html">Services</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="portfolio.html">Portfolio</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="blog.html">Blog</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="contact.html">Contact</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="elements.html">Elements</a>
          </li>
        </ul>
      </nav>
    </div>
    <!-- Copwrite Text -->
    <div class="copywrite-text">
      <p>
        <!-- Link back to Colorlib can't be removed. Template is licensed under CC BY 3.0. -->
        Copyright &copy; {{currentYear}} All rights reserved | This template is made with
        <i class="fa fa-heart-o" aria-hidden="true"></i> by
        <a href="https://colorlib.com" target="_blank">Colorlib</a>
        <!-- Link back to Colorlib can't be removed. Template is licensed under CC BY 3.0. -->
      </p>
    </div>
  </div>
  <!-- ***** Main Menu Area End ***** -->
</template>

<script>
export default {
  computed: {
    currentYear() {
      return new Date().getFullYear()
    },
  },
};
</script>
