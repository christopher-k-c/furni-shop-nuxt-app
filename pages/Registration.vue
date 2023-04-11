<!-- Registration.vue -->

<template>
    <div>
      <Nav /> <!-- Include Nav component -->
      <h1>Registration Page</h1>
      <!-- Registration page content goes here -->
      <Footer /> <!-- Include Footer component -->
    </div>
  </template>
  
  <script>
  import Nav from '@/components/Nav.vue'; // Import Nav component
  import Footer from '@/components/Footer.vue'; // Import Footer component
  
  export default {
    components: {
      Nav,
      Footer,
    },
  };
  </script>
  
  <style scoped>
  /* Registration page styles go here */
  </style>
  