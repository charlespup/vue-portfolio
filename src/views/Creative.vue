<template>
  <div class="container py-5">
    <Navbar/>
    <h2 class="text-center mb-4 text-white">Creative Corner</h2>
    
    <div class="row g-4">
      <div class="col-md-6">
        <div class="card h-100 p-3 text-white">
          <h5 class="mb-3 text-white">📸 Photography</h5>
          <p>I enjoy capturing cityscapes and landscapes, especially during golden hour. It helps me relax and notice details in my surroundings.</p>
        </div>
      </div>
      
      <div class="col-md-6">
        <div class="card h-100 p-3 text-white">
          <h5 class="mb-3 text-white">📝 Blog: Learning Vue</h5>
          <p>Started my journey into Vue.js recently. I love how reactive data binding works and how Vue Router makes SPA routing easy!</p>
        </div>
      </div>
      
      <div class="col-md-6">
        <div class="card h-100 p-3 text-white">
          <h5 class="mb-3 text-white">🎮 Gaming</h5>
          <p>I play strategy and simulation games. They challenge my thinking and help me unwind after classes or projects.</p>
        </div>
      </div>
      
      <div class="col-md-6">
        <div class="card h-100 p-3">
          <h5 class="mb-3 text-white">💡 Project Ideas</h5>
          <ul class="text-white">
            <li>Smart helmet for construction safety</li>
            <li>AI voice assistant for visually impaired</li>
            <li>IoT trash bin with solar sensors</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from '../components/Navbar.vue';
export default {
  name: 'CreativePage',
  components: {
    Navbar
  }
};
</script>

