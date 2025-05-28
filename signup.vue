<template>
  <div class="signup-container">
    <h2>Admin Sign Up</h2>
    <form @submit.prevent="handleSignUp">
      <div class="form-group">
        <label for="username">Username:</label>
        <input id="username" v-model="username" type="text" required />
      </div>
      <div class="form-group">
        <label for="email">Email:</label>
        <input id="email" v-model="email" type="email" required />
      </div>
      <div class="form-group">
        <label for="password">Password:</label>
        <input id="password" v-model="password" type="password" required />
      </div>
      <button type="submit">Sign Up</button>
    </form>
    <p>
      Already have an account?
      <a href="./login.vue">Login here</a>
    </p>
  </div>
</template>

<script>
export default {
  name: "AdminSignUp",
  data() {
    return {
      username: "",
      email: "",
      password: ""
    };
  },
  methods: {
    handleSignUp() {
      alert(`Sign Up submitted for username: ${this.username}, email: ${this.email}`);
      // Add actual sign up logic here
    }
  }
};
</script>

<style scoped>
.signup-container {
  max-width: 400px;
  margin: 2rem auto;
  padding: 1rem;
  border: 1px solid #ccc;
  border-radius: 8px;
}
.form-group {
  margin-bottom: 1rem;
}
label {
  display: block;
  margin-bottom: 0.3rem;
}
input {
  width: 100%;
  padding: 0.4rem;
  box-sizing: border-box;
}
button {
  background-color: #007bff;
  color: white;
  border: none;
  padding: 0.6rem 1.2rem;
  border-radius: 4px;
  cursor: pointer;
}
button:hover {
  background-color: #0056b3;
}
a {
  color: #007bff;
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}
</style>
