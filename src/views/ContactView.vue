<template>
  <NavbarComponent />
  <div class="container rounded mt-5 pt-5">
    <div class="row">
      <!-- Left Column: Contact Form -->
      <div class="col-md-6">
        <h2 class="mb-4">Contact Me</h2>
        <form @submit.prevent="submitForm" class="pb-5">
          <!-- Name Field -->
          <div class="mb-3">
            <label for="name" class="form-label">Name</label>
            <input v-model="form.name" type="text" class="form-control" id="name" placeholder="Your name" required />
          </div>

          <!-- Email Field -->
          <div class="mb-3">
            <label for="email" class="form-label">Email address</label>
            <input v-model="form.email" type="email" class="form-control" id="email" placeholder="name@example.com"
              required />
          </div>

          <!-- Subject Field -->
          <div class="mb-3">
            <label for="subject" class="form-label">Subject</label>
            <input v-model="form.subject" type="text" class="form-control" id="subject" placeholder="Subject" />
          </div>

          <!-- Message Field -->
          <div class="mb-3">
            <label for="message" class="form-label">Message</label>
            <textarea v-model="form.message" class="form-control" id="message" rows="5" placeholder="Your message here"
              required></textarea>
          </div>

          <!-- Submit Button -->
          <button type="submit" class="btn btn-success">Send Message</button>
        </form>
      </div>

      <!-- Right Column: Alternative Contact Information -->
      <div class="col-md-6">
        <h2 class="mb-4">Other Ways to Reach Me</h2>
        <p>If you prefer, you can also contact me via:</p>
        <ul class="list-unstyled">
          <li>
            <strong>Email: </strong>
            <a href="mailto:lagmayravenglenn73@gmail.com">lagmayravenglenn73@gmail.com</a>
          </li>
          <li>
            <strong>Phone: </strong>
            <a href="tel:+639765350942">+63976-535-0942</a>
          </li>
          <li>
            <strong>LinkedIn: </strong>
            <a href="https://www.linkedin.com/in/raven-glenn-lagmay-3a985b27b/" target="_blank">
              View my profile
            </a>
          </li>
          <!-- Add more contact methods as needed -->
        </ul>
        <p>
          Feel free to reach out using any of the above methods, and I'll get
          back to you as soon as possible!
        </p>
      </div>
    </div>
  </div>
  <FooterComponent class="mt-5" />
</template>

<script>
export default {
  name: "Contact",
  data() {
    return {
      form: {
        name: "",
        email: "",
        subject: "",
        message: ""
      }
    };
  },
  methods: {
    submitForm() {
      console.log("Form submitted:", this.form);
      // Reset form fields
      this.form = {
        name: "",
        email: "",
        subject: "",
        message: ""
      };
      alert("Thank you! Your message has been sent.");
    }
  }
};
</script>

<style scoped>
.container {
  border: 1px solid #ccc;
  background-color: white;
  padding: 2rem;
}
</style>
