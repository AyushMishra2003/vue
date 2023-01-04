<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-light bg-light fixed-top">
      <div class="container">
        <NuxtLink class="navbar-brand" to="/"
          ><img
            src="/img/logo/logo.png"
            alt="Logo"
            class="img-fluid"
            width="100"
        /></NuxtLink>
        <button
          class="navbar-toggler"
          type="button"
          data-mdb-toggle="collapse"
          data-mdb-target="#navbarTogglerDemo02"
          aria-controls="navbarTogglerDemo02"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <i class="fas fa-bars"></i>
        </button>
        <div class="collapse navbar-collapse" id="navbarTogglerDemo02">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <NuxtLink class="nav-link" to="/">Home</NuxtLink>
            </li>
            <li class="nav-item">
              <NuxtLink class="nav-link" to="/about-us/">About Us</NuxtLink>
            </li>
            <!-- Dropdown -->
            <li class="nav-item dropdown">
              <a
                class="nav-link dropdown-toggle"
                href="#"
                id="navbarDropdownMenuLink"
                role="button"
                data-mdb-toggle="dropdown"
                aria-expanded="false"
              >
                Services
              </a>
              <ul
                class="dropdown-menu services_menu"
                aria-labelledby="navbarDropdownMenuLink"
              >
                <li>
                  <NuxtLink class="dropdown-item services_item" to="#"
                    >Local Car Rental</NuxtLink
                  >
                </li>
                <li>
                  <NuxtLink class="dropdown-item services_item" to="#"
                    >Outstation Car Rental</NuxtLink
                  >
                </li>
                <li>
                  <NuxtLink class="dropdown-item services_item" to="#"
                    >Corporate Car Rental</NuxtLink
                  >
                </li>
                <li>
                  <NuxtLink class="dropdown-item services_item" to="#"
                    >Wedding/Event/Conference</NuxtLink
                  >
                </li>
                <li>
                  <NuxtLink class="dropdown-item services_item" to="#"
                    >Airport/Railway Stn./Employee Transfer
                  </NuxtLink>
                </li>
                <li>
                  <NuxtLink class="dropdown-item services_item" to="#"
                    >Car Rental on Monthly Basis
                  </NuxtLink>
                </li>
              </ul>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Rate Chart</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Contact Us</a>
            </li>
          </ul>
          <div class="d-flex align-items-center">
            <a
              href="tel:+919520801801"
              class="btn btn-rounded"
              target="_blank"
              role="button"
            >
              <i class="fa-solid fa-phone me-1 text-white"></i> +91 95208 01801
            </a>
            <a
              href="#"
              class="btn btn-floating ms-2"
              target="_blank"
              role="button"
              style="background-color: #3b5998"
            >
              <i class="fab fa-facebook-f fa-lg text-white"></i>
            </a>
            <a
              href="#"
              class="btn btn-floating ms-2 instagram"
              target="_blank"
              role="button"
            >
              <i class="fab fa-instagram fa-lg text-white"></i>
            </a>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {};
</script>

<style scoped></style>
