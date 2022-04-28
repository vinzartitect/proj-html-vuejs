<template>
  <section>
    <!-- SECTION About Jumbo -->
    <section id="about" class="border-bottom">
      <div class="container p-5 mb-5">
        <div class="row align-items-center">
          <!-- testo a sinistra -->
          <div id="about-text" class="col-12 col-md-6">
            <span
              class="d-inline-block my-blue-text my-alice-blue-bg border fw-bold rounded-pill mb-3"
              >Development</span
            >
            <h1 class="mb-4 fw-bold">A Complete<br />Developer Toolset</h1>
            <p class="mb-4 text-secondary">
              Launch your campaign and benefit from our expertise on designing
              and managing conversion centered bootstrap4 html page.
            </p>
            <div class="mb-4 fw-bold">
              <a
                class="me-3 text-decoration-none p-2 text-white my-blue-bg rounded shadow"
                href="#"
                >Get Started</a
              >
              <a class="text-decoration-none p-2 my-blue-text rounded" href="#"
                >Documentation</a
              >
            </div>
            <p class="text-secondary">Current Version: v2.6.0</p>
          </div>
          <!-- fine testo a sinistra -->

          <!-- immagine a destra -->
          <div class="col-12 col-md-6 d-flex justify-content-center">
            <img
              class="img-fluid"
              src="../assets/img/about.png"
              alt="ragazzo seduto al pc"
            />
          </div>
          <!-- fine immagine a destra -->
        </div>
      </div>
    </section>
    <!-- fine SECTION About Jumbo -->

    <!-- SECTION sponsor brands -->
    <section id="sponsor-brands" class="my-light-gray-bg p-5 mb-5">
      <div class="container">
        <div class="row">
          <img
            class="col-2"
            v-for="(sponsor, index) in sponsorBrands"
            :key="index"
            :src="require(`../assets/img/${sponsor.logo}`)"
            :alt="sponsor.name + ' ' + 'logo'"
          />
        </div>
      </div>
    </section>
    <!-- fine SECTION sponsor brands -->
  </section>
</template>

<script>
export default {
  name: "AboutSection",
  data: function () {
    return {
      /* array sponsor */
      sponsorBrands: [
        {
          name: "Amazon",
          logo: "amazon.svg",
        },
        {
          name: "Google",
          logo: "google.svg",
        },
        {
          name: "Lenovo",
          logo: "lenovo.svg",
        },
        {
          name: "PayPal",
          logo: "paypal.svg",
        },
        {
          name: "Shopify",
          logo: "shopify.svg",
        },
        {
          name: "Spotify",
          logo: "spotify.svg",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../assets/scss/partials/_colors.scss";
section#about {
  padding-top: 100px;
  background-color: $fondoschermo;

  div#about-text span {
    font-size: 0.8rem;
    padding: 0.3rem;
  }

  div#about-text a {
    border: 1px solid #2f55d4;
  }

  div#about-text a:hover {
    color: white;
    background-color: #2844aa;
    border: 1px solid #2844aa;
  }
}

section#sponsor-brands {
  border-radius: 0 0 45% 45%;

  img {
    height: 30px;
  }
}
</style>
