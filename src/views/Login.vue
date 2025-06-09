<template>
  <div class="container vh-100 d-flex justify-content-center align-items-center text-white">
    <div class="card p-4 w-100" style="max-width: 400px;">
      <h3 class="text-center mb-3 text-white">Login</h3>
      <form @submit.prevent="login">
        <div class="mb-3">
          <input v-model="username" type="text" class="form-control" placeholder="Username" required>
        </div>
        <div class="mb-3">
          <input v-model="password" type="password" class="form-control" placeholder="Password" required>
        </div>
        <button type="submit" class="btn btn-custom w-100">Login</button>
        <p class="text-danger mt-2" v-if="error">Invalid credentials</p>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LoginPage',
  data() {
    return {
      username: '',
      password: '',
      error: false
    };
  },
  methods: {
    login() {
      if (this.username === 'admin' && this.password === 'admin') {
        this.$router.push('/portfolio/profile');
      } else {
        this.error = true;
      }
    }
  }
};
</script>