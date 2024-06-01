<template>
    <nav class="navbar">
      <h1>Logo</h1>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </template>
  
  <script>
  export default {
    name: 'Navbar'
  }
  </script>
  
  <style scoped lang="scss">
  @import '../styles/variables.scss';
  
  .navbar {
    background-color: $primary-color;
    padding: 1rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    h1 {
      color: $text-color;
    }
    ul {
      list-style: none;
      display: flex;
      gap: 1rem;
      li {
        a {
          color: $text-color;
          text-decoration: none;
        }
      }
    }
  }
  </style>
  