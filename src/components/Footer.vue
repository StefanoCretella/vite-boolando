<template>
    <footer class="footer">
      <p>&copy; 2024 Boolando. Tutti i diritti riservati.</p>
    </footer>
  </template>
  
  <script>
  export default {
    name: 'Footer'
  }
  </script>
  
  <style scoped lang="scss">
  @import 'src/assets/styles/variables.scss';
  
  .footer {
    background-color: $primary-color;
    padding: 1rem;
    p {
      color: $text-color;
    }
  }
  </style>
  