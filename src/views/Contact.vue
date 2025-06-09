<template>
  <div class="container py-5">
    <Navbar/>
    <h2 class="text-center mb-4 text-white">Contact Me</h2>
    
    <div class="card p-4 mx-auto" style="max-width: 600px;">
      <form @submit.prevent="submitForm">
        <div class="mb-3 text-white">
          <label for="name" class="form-label">Name</label>
          <input v-model="form.name" type="text" class="form-control" id="name" required>
        </div>
        
        <div class="mb-3 text-white">
          <label for="email" class="form-label">Email</label>
          <input v-model="form.email" type="email" class="form-control" id="email" required>
        </div>
        
        <div class="mb-3 text-white">
          <label for="message" class="form-label">Message</label>
          <textarea v-model="form.message" class="form-control" id="message" rows="4" required></textarea>
        </div>
        
        <button type="submit" class="btn btn-custom w-100">Send</button>
        <p class="text-success mt-3" v-if="submitted">Message sent successfully!</p>
      </form>
    </div>
  </div>
</template>

<script>
import Navbar from '../components/Navbar.vue';
export default {
  name: 'ContactPage',
  components: {
    Navbar
  },
  data() {
    return {
      form: {
        name: '',
        email: '',
        message: ''
      },
      submitted: false
    };
  },
  methods: {
    submitForm() {
      // You can replace this with actual API/email logic later
      console.log("Message submitted:", this.form);
      this.submitted = true;
      this.form = { name: '', email: '', message: '' };
    }
  }
};
</script>

