<template>
  <div class="my-5">
    <!-- hero -->
    <section class="chardham_hero d-flex align-items-center">
      <div class="container text-capitalize display-4 text-center">
        <p class="text-white">
          book hassle free chardham yatra 2023 with UCS Cab
        </p>
        <a
          href="tel:+919520801801"
          class="btn btn-rounded fs-6"
          target="_blank"
          role="button"
        >
          <i class="fa-solid fa-phone me-1 text-white"></i> +91 95208 01801
        </a>
      </div>
    </section>

    <!-- rates -->
    <section class="my-5 py-md-5 container">
      <h3 class="fw-bold">Taxi Fare for Chardham Yatra 2023:</h3>
      <div class="table-responsive">
        <table class="table table-striped table-hover mt-4">
          <thead>
            <tr>
              <th scope="col" class="fw-bold fs-5 text-white">Cab / Taxi</th>
              <th scope="col" class="fw-bold fs-5 text-white">Tariff</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <th scope="row">Sedan</th>
              <td>₹ 4500/- Per Day</td>
            </tr>
            <tr>
              <th scope="row">Mini SUV</th>
              <td>₹ 5500/ - Per Day</td>
            </tr>
            <tr>
              <th scope="row">SUV</th>
              <td>₹ 6500/- Per Day</td>
            </tr>
            <tr>
              <th scope="row">Premium SUV</th>
              <td>₹ 7000/- Per Day</td>
            </tr>
          </tbody>
        </table>
      </div>
      <div class="text-center mt-5">
        <a
          href="tel:+919520801801"
          class="btn btn-rounded fs-5"
          target="_blank"
          role="button"
        >
          <i class="fa-solid fa-phone me-1 text-white"></i> book now with UCS
          Cab
        </a>
      </div>
    </section>

    <!-- tour content -->
    <section class="py-5 tour_content">
      <div class="container py-5">
        <div class="row g-5">
          <div class="col-md-6 my-auto">
            <h3 class="fw-bold">
              Make the Most of your Chardham Yatra Tour with UCS Cab
            </h3>
            <p class="mt-4">
              Planning for your Chardham yatra this year? You have knocked on
              the right door. UCS Cab will ensure that your tour of four holy
              sites is seamless. Among the countless religious sites and
              circuits that devotees visit in Uttarakhand, one of the most
              prominent is the Uttarakhand Chardham yatra.
            </p>
          </div>
          <div class="col-md-6">
            <nuxt-img preset="cover"
              src="/kedarnath.jpg"
              alt="Mountains"
              class="img-fluid rounded"
            />
          </div>
        </div>
      </div>
      <div class="text-center mt-4">
        <a
          href="tel:+919520801801"
          class="btn btn-rounded fs-5"
          target="_blank"
          role="button"
        >
          <i class="fa-solid fa-phone me-1 text-white"></i> book now with UCS
          Cab
        </a>
      </div>
    </section>

    <!-- why choose -->
    <section class="my-5 py-md-5 container">
      <h3 class="fw-bold">Why should you do Chardham Yatra?</h3>
      <p class="mt-4">
        In Hinduism, Teerth Yatra is one of the five duties of every Hindu. The
        other four duties are Dharma, Worship, Sanskaras, and Observing
        religious festivals. It is believed that every Hindu must visit this
        pilgrimage once in their lifetime as the Yatra helps in attaining
        salvation or what is known as Moksha by washing away the sins.
      </p>

      <h3 class="fw-bold mt-5">Char Dham Yatra</h3>
      <p class="mt-4">
        The Char Dhams generally include four sacred temples, Badrinath,
        Kedarnath, Gangotri and Yamunotri.
      </p>
      <ul>
        <li>
          <span class="fw-bold">Bardinath</span>: The Badrinath temple is the
          home of Lord Vishnu and is the pilgrim centres in the Uttarakhand.
        </li>
        <li>
          <span class="fw-bold">Kedarnath</span>: Kedarnath temple is the home
          of Lord Shiva and is located in the Rudraprayag District of
          Uttarakhand.
        </li>
        <li>
          <span class="fw-bold">Gangotri</span>: Gangotri temple is situated
          near a sacred rock where Bhagiratha worshipped Shiva and is dedicated
          to Goddess Ganga.
        </li>
        <li>
          <span class="fw-bold">Yamunotri</span>: Yamunotri temple is located in
          Uttarakashi and is the home of Goddess Yamuna.
        </li>
      </ul>
      <div class="text-center mt-5">
        <a
          href="tel:+919520801801"
          class="btn btn-rounded fs-5"
          target="_blank"
          role="button"
        >
          <i class="fa-solid fa-phone me-1 text-white"></i> book now with UCS
          Cab
        </a>
      </div>
    </section>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.chardham_hero {
  background: linear-gradient(rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.2)),
    url("/chardham-hero.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  height: 700px;
}

.chardham_hero div p {
  font-weight: 600;
}

thead {
  background-color: #2399c0;
}

.tour_content {
  background-color: #f9fafb;
}

@media screen and (max-width: 768px) {
  .chardham_hero {
    height: 300px;
  }
}
</style>
