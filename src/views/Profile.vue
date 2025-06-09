<template>
  <div class="container py-5">
    <Navbar/>
    <div class="card text-center p-4 mx-auto" style="max-width: 600px;">
      <img src="@/assets/profile.jpg" alt="Profile Photo" class="rounded-circle mx-auto mb-3" width="150" height="150">
      
      <h3 class="mb-2 text-white">Charles Christian F. Marin</h3>
      
      <!-- Typed text will animate inside this span -->
      <p class="text-white">
        <span ref="typedText"></span>
      </p>

      <div class="text-start mt-4 px-3">
        <p class="text-white"><strong>Age:</strong> 22</p>
        <p class="text-white"><strong>University:</strong> Polytechnic University of the Philippines Sta. Mesa</p>
        <p class="text-white"><strong>Email:</strong> charlesmarin57@gmail.com</p>
        <p class="text-white"><strong>Phone:</strong> +63 969 087 6125</p>

        <div class="d-flex justify-content-center mt-3">
          <a href="https://github.com/yourusername" target="_blank" class="btn btn-custom btn-sm mx-1">
            <i class="bi bi-facebook"></i> Facebook
          </a>
          <a href="https://linkedin.com/in/yourusername" target="_blank" class="btn btn-custom btn-sm mx-1">
            <i class="bi bi-instagram"></i> Instagram
          </a>
          <a href="mailto:charlesmarin57@gmail.com" class="btn btn-custom btn-sm mx-1">
            <i class="bi bi-envelope"></i> Email
          </a>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import Navbar from '../components/Navbar.vue';
import Typed from 'typed.js';

export default {
  name: 'ProfilePage',
  components: {
    Navbar
  },
  mounted() {
    const options = {
      strings: [
        "Computer Engineering Student",
        "Tech Enthusiast",
        "Passionate About Networking",
        "Driven by Innovation",
      ],
      typeSpeed: 50,
      backSpeed: 30,
      loop: true
    };

    new Typed(this.$refs.typedText, options);
  }
};
</script>


<style scoped>
img {
  object-fit: cover;
  border: 3px solid #f1c40f;
}
</style>

