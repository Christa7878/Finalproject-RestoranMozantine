<script setup>
import Data from "./assets/data";
import DataBarang from "./assets/dataBarang";
</script>
<script>
export default {
  data: function () {
    return {
      content: Data,
      titleHero: "Finest italian food for your taste",
    };
  },
  methods: {
    changeTitle(data) {
      this.titleHero = data.nama;
      this.titleImage = data.image;
    },
  },
};
</script>

<template>
  <!-- Area Navbar -->
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container">
      <a class="navbar-brand" href="">Mozantine </a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarTogglerDemo02"
        aria-controls="navbarTogglerDemo02"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarTogglerDemo02">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item">
            <a class="nav-link" href="">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="">Menu</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="">Contact</a>
          </li>
          <li class="nav-item me-3 mb-lg-0 me-lg-5">
            <a class="nav-link" href="">About Us</a>
          </li>
          <li class="nav-item me-2">
            <form class="nav-item" role="search">
              <input
                type="search"
                class="form-control form-control-dark text-bg-dark"
                placeholder="Search..."
                aria-label="Search"
              />
            </form>
          </li>
          <li class="nav-item me-2">
            <a class="nav-item" href=""
              ><button
                type="button"
                style="background-color: #3aae4d; border-color: #3aae4d"
                class="btn btn-warning"
              >
                Log in
              </button></a
            >
          </li>
          <li class="nav-item me-2">
            <a class="nav-item" href=""
              ><button type="button" class="btn btn-outline-light">
                <img
                  src="./assets/shoppingcart_icon.png"
                  alt="icon shopping cart"
                  style="height: 20px"
                /></button
            ></a>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- opsi image1 -->
  <!-- <div class=""></div>
  <div class="container2">
    <img
      src="./assets/bannerBG1.jpg"
      class="banner_top_image"
      alt="banner img top"
      style="width: 100rem"
    /> -->

  <!-- opsi image 2 yang responsive -->
  <div class=""></div>
  <div class="container2">
    <img src="./assets/bannerBG1.jpg" class="img-fluid" alt="banner img top" />
  </div>
  <!-- image ends here -->

  <div class="px-4 py-5 my-5 text-center">
    <h1 class="display-5 fw-bold">{{ titleHero }}</h1>
    <div class="col-lg-6 mx-auto">
      <p class="lead mb-4">
        Best handpicked ingredients from local farmers and cooked with
        experienced Italian chefs.
      </p>
      <div class="d-grid gap-2 d-sm-flex justify-content-sm-center">
        <button
          type="button"
          style="background-color: #3aae4d; border-color: #3aae4d"
          class="btn btn-primary btn-lg px-4 gap-3"
        >
          Start order
        </button>
      </div>
    </div>
  </div>

  <!-- Ini area superb taste and experience -->

  <div class="container">
    <h3 class="display-5 fw-bold">
      <span style="color: #3aae4d">Superb </span>Taste And Experience
    </h3>
    <p></p>
    <div class="row">
      <div class="col mt-5" v-for="data in Data">
        <div class="card" style="width: 18rem">
          <img :src="data.image" class="card-img-top" alt="..." />
          <div class="card-body text-center">
            <h5 class="card-title title-name">{{ data.nama }}</h5>
            <p class="card-text subtitle-name">{{ data.keterangan }}</p>
            <button
              @click="changeTitle(data)"
              href="#"
              style="background-color: #3aae4d; border-color: #3aae4d"
              class="btn btn-primary"
            >
              View Menu
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Ini area chef recommendation -->

  <br />
  <br />
  <br />
  <br />

  <div class="container">
    <h3 class="display-5 fw-bold">
      <span style="color: #3aae4d">Chef </span>Recommendation
    </h3>
    <div class="row">
      <div class="col mt-5" v-for="dataBarang in DataBarang">
        <div class="card" style="width: 18rem">
          <img :src="dataBarang.image" class="card-img-top" alt="..." />
          <div class="card-body text-center">
            <h5 class="card-title title-name">{{ dataBarang.nama }}</h5>
            <p class="card-text subtitle-name">{{ dataBarang.harga }}</p>
            <button
              @click="changeTitle(data)"
              href="#"
              style="background-color: #3aae4d; border-color: #3aae4d"
              class="btn btn-primary"
            >
              Add to basket
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- ini area footer -->

  <br />
  <br />

  <div class="container">
    <footer class="py-5">
      <div class="row">
        <div class="col-6 col-md-2 mb-3">
          <h5>About Us</h5>
          <ul class="nav flex-column">
            <li class="nav-item mb-2">
              <a href="#" class="nav-link p-0 text-muted">Profile</a>
            </li>
            <li class="nav-item mb-2">
              <a href="#" class="nav-link p-0 text-muted">Menu</a>
            </li>
            <li class="nav-item mb-2">
              <a href="#" class="nav-link p-0 text-muted">Location</a>
            </li>
            <li class="nav-item mb-2">
              <a href="#" class="nav-link p-0 text-muted">Contact Us</a>
            </li>
          </ul>
        </div>

        <div class="col-6 col-md-2 mb-3">
          <h5>My Account</h5>
          <ul class="nav flex-column">
            <li class="nav-item mb-2">
              <a href="#" class="nav-link p-0 text-muted">Sign up</a>
            </li>
            <li class="nav-item mb-2">
              <a href="#" class="nav-link p-0 text-muted">My Point</a>
            </li>
            <li class="nav-item mb-2">
              <a href="#" class="nav-link p-0 text-muted">Saved Address</a>
            </li>
          </ul>
        </div>

        <div class="col-6 col-md-2 mb-3">
          <h5>Follow Us</h5>
          <ul class="nav flex-column">
            <li class="nav-item mb-2">
              <a href="#" class="nav-link p-0 text-muted">Instagram</a>
            </li>
            <li class="nav-item mb-2">
              <a href="#" class="nav-link p-0 text-muted">Facebook</a>
            </li>
            <li class="nav-item mb-2">
              <a href="#" class="nav-link p-0 text-muted">Twitter</a>
            </li>
          </ul>
        </div>

        <div class="col-md-5 offset-md-1 mb-3">
          <form>
            <h5>Subscribe to our newsletter</h5>
            <p>
              Monthly menu recommendation, discount promo and exciting news from
              Mozantine.
            </p>
            <div class="d-flex flex-column flex-sm-row w-100 gap-2">
              <label for="newsletter1" class="visually-hidden"
                >Email address</label
              >
              <input
                id="newsletter1"
                type="text"
                class="form-control"
                placeholder="Email address"
              />
              <button
                class="btn btn-primary"
                style="background-color: #3aae4d; border-color: #3aae4d"
                type="button"
              >
                Subscribe
              </button>
            </div>
          </form>
        </div>
      </div>

      <div
        class="d-flex flex-column flex-sm-row justify-content-between py-4 my-4 border-top"
      >
        <p>© 2022 Mozantine All rights reserved.</p>
      </div>
    </footer>
  </div>
</template>

<style scoped>
header {
  line-height: 1.5;
}
div.scrollmenu {
  background-color: #333;
  overflow: auto;
  white-space: nowrap;
}

div.scrollmenu a {
  display: inline-block;
  color: white;
  text-align: center;
  padding: 14px;
  text-decoration: none;
}

div.scrollmenu a:hover {
  background-color: #777;
}
.title-name {
  color: black;
  text-transform: capitalize;
}
.subtitle-name {
  color: grey;
}

.banner_top_image {
  position: relative;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

.outsideContainer {
  position: absolute;
  top: 0;
  width: 100vw;
  height: 100vh;
  background-color: rgba(0, 0, 0, 0.8);
  visibility: hidden;
  opacity: 0;
  transition-property: all;
  transition-duration: 1s;
  z-index: 10;
}
.containerModal {
  background-color: white;
  padding: 20px;
  color: black;

  width: 100%;
  z-index: 10;
  width: 400px;
  height: 400px;
  margin: 40vh auto;
}
.containerModal img {
  height: 300px;
}
.outsideContainer.shown {
  visibility: visible;
  opacity: 1;
}
@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}

@import url("https://fonts.googleapis.com/css?family=Open+Sans");

body {
  display: flex;
  background-color: #f0f8ff;
  height: 95vh;
  justify-content: center;
  align-items: flex-end;
  font-family: Open Sans;
}

#container {
  padding-top: 20px;
  margin-top: 20px;
  width: 100vw;
  color: white;
  background-color: #292354;
  display: flex;
  flex-direction: column;
  align-items: center;
}

#container2 {
  padding-top: 20px;
}

#contacts {
  display: flex;
  justify-content: space-around;
  align-items: center;
  width: 100%;
}
#contacts--contact {
  text-align: right;
}
#contacts--social {
  width: 20%;
  display: flex;
  justify-content: space-between;
}
#contacts--social div {
  height: 30px;
  width: 30px;
  background-color: white;
  border-radius: 50%;
}
#mentions p {
  font-size: 0.5em;
}
</style>
