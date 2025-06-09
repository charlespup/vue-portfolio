<template>
  <div class="container py-5">
    <Navbar/>
    <h2 class="text-center mb-4 text-white">My Projects</h2>
    <div class="row g-4">
      <div class="col-md-4" v-for="(project, index) in projects" :key="index">
        <div class="card h-100">
          <div class="card-body text-white">
            <h5 class="card-title">{{ project.title }}</h5>
            <p class="card-text">{{ project.description }}</p>
          </div>
          <div class="card-footer bg-transparent border-0">
            <a :href="project.link" target="_blank" class="btn btn-custom w-100">View Project</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from '../components/Navbar.vue';
import VanillaTilt from 'vanilla-tilt';

export default {
  name: 'ShowcasePage',
  components: {
    Navbar
  },
  data() {
    return {
      projects: [
        {
          title: 'FountainPaws IoT System',
          description: 'An IoT-based cat water monitoring project using flowing vs. still water bowls.',
          link: 'https://github.com/yourusername/fountainpaws'
        },
        {
          title: 'QR Inventory System',
          description: 'QR Code-Powered Inventory System for PUP’s PSMO office.',
          link: 'https://github.com/yourusername/telliScan'
        },
        {
          title: 'LoRa Emergency Device',
          description: 'Solar-powered LoRa GPS device for post-typhoon search and rescue.',
          link: 'https://github.com/yourusername/lora-rescue'
        }
      ]
    };
  },
  mounted() {
    // Apply tilt effect to each card
    const elements = this.$el.querySelectorAll('.card');
    VanillaTilt.init(elements, {
      max: 15,
      speed: 400,
      glare: true,
      "max-glare": 0.2
    });
  }
};
</script>


<style scoped>
.card-img-top {
  height: 200px;
  object-fit: cover;
}
</style>

