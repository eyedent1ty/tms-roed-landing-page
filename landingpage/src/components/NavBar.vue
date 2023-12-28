<script>
export default {
    name: 'NavBar'
};
</script>

<template>
      <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container nav-con">
          <a class="navbar-brand" href="#homeSection">
            <img
              src="../assets/company_logo.png"
              height="50"
              alt="company logo"
            />
            RO-ED Logistics and Services
          </a>


          <button
            class="navbar-toggler"
            type="button"
            data-bs-toggle="collapse"
            data-bs-target="#navbarNav"
            aria-controls="navbarNav"
            aria-expanded="false"
            aria-label="Toggle navigation"
          >
            <span class="navbar-toggler-icon"></span>
          </button>

          <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav ms-auto">
              <li class="nav-item">
                <a class="nav-link" href="#homeSection">Home</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#aboutUsSection">About Us</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#clientsSection">Clients</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#contactSection">Contact Us</a>
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
</style>
