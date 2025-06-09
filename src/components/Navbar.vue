<template>
  <nav class="navbar navbar-expand-lg navbar-dark">
    <div class="container">
      <router-link class="navbar-brand text-warning" to="/portfolio/profile">My Portfolio</router-link>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item">
            <router-link class="nav-link" to="/portfolio/profile">Profile</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/portfolio/showcase">Showcase</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/portfolio/contact">Contact</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/portfolio/creative">Creative</router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'MainNavbar'
};
</script>

<style scoped>
.navbar-brand {
  font-weight: bold;
  font-size: 1.5rem;
}
</style>