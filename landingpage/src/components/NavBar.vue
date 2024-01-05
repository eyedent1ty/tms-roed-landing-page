<script>
export default {
    name: 'NavBar'
};
</script>

<template>
  <nav class="navbar navbar-expand-lg">
    <div class="container nav-con d-flex justify-content-between">
      <div class="d-flex align-items-center">
        <img src="../assets/company_name_logo.png" height="50" alt="Company Name & Logo" />

        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
          aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
      </div>

      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item">
            <a class="nav-link" href="#homeSection">
              <h5>Home</h5>
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#aboutUsSection">
              <h5>About Us</h5>
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#clientsSection">
              <h5>Clients</h5>
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#contactSection">
              <h5>Contact Us</h5>
            </a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style scoped>
    .navbar .nav-con{
        width: 100vh;
    }

    .nav-item {
        display: flex; 
        justify-content: center; 
        align-items: center; 
    }

    .nav-link:hover {
      color: white;
      text-shadow: 2px 2px 4px #000000;
    }
</style>
